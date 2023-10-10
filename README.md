# ModifiedMeshGraphNet

.pt data is in DATA/flag_simple_test
notebook used to create .pt data is in "data creation"

Model ran using this format
python -m run_model --mode=train --model=cloth --dataset=flag_simple

After Running "runmodel.py" Should result in the following output and error

I1009 17:43:32.890568 179756 run_model.py:722] =========================================================
I1009 17:43:32.890568 179756 run_model.py:723] Start new run in C:\Users\trist\.conda\meshgraphnets-main _modified\output\flag_simple\Mon-Oct--9-17-43-32-2023\1
I1009 17:43:32.890568 179756 run_model.py:724] =========================================================
I1009 17:43:32.891565 179756 run_model.py:736] Program started at time Mon Oct  9 17:43:32 2023
I1009 17:43:32.891565 179756 run_model.py:740] Start training......
C:\Users\trist\anaconda3\Lib\site-packages\torch\nn\modules\lazy.py:180: UserWarning: Lazy modules are a new feature under heavy development so changes to the API or functionality can happen at any moment.
  warnings.warn('Lazy modules are a new feature under heavy development '
I1009 17:43:33.009250 179756 run_model.py:640] 
I1009 17:43:33.009250 179756 run_model.py:641] =======================Run Summary=======================
I1009 17:43:33.009250 179756 run_model.py:642] Simulation task is cloth simulation
I1009 17:43:33.009250 179756 run_model.py:643] Mode is train
I1009 17:43:33.009250 179756 run_model.py:647] No Evaluation
I1009 17:43:33.010248 179756 run_model.py:648] Train and/or evaluation configuration are 2 epochs, 2 trajectories each epoch, number of rollouts is 1
I1009 17:43:33.015235 179756 run_model.py:652] Core model is encode_process_decode
I1009 17:43:33.015235 179756 run_model.py:653] Message passing aggregator is sum
I1009 17:43:33.015235 179756 run_model.py:654] Message passing steps are 5
I1009 17:43:33.015235 179756 run_model.py:655] Attention used is False
I1009 17:43:33.015235 179756 run_model.py:656] Ripple used is False
I1009 17:43:33.016232 179756 run_model.py:665] Run output directory is C:\Users\trist\.conda\meshgraphnets-main _modified\output\flag_simple\Mon-Oct--9-17-43-32-2023\1
I1009 17:43:33.016232 179756 run_model.py:666] =========================================================
I1009 17:43:33.016232 179756 run_model.py:667]
I1009 17:43:34.349669 179756 run_model.py:339] Epoch 1/2
I1009 17:43:34.349669 179756 run_model.py:345] Training with 1 GPUs
I1009 17:43:34.349669 179756 run_model.py:348]     trajectory index 1/2
Traceback (most recent call last):
  File "<frozen runpy>", line 198, in _run_module_as_main
  File "<frozen runpy>", line 88, in _run_code
  File "C:\Users\trist\.conda\meshgraphnets-main _modified\run_model.py", line 1083, in <module>
    app.run(main)
  File "C:\Users\trist\anaconda3\Lib\site-packages\absl\app.py", line 312, in run
    _run_main(main, args)
  File "C:\Users\trist\anaconda3\Lib\site-packages\absl\app.py", line 258, in _run_main
    sys.exit(main(argv))
             ^^^^^^^^^^
  File "C:\Users\trist\.conda\meshgraphnets-main _modified\run_model.py", line 765, in main
    train_loss_record = learner(model, params, run_step_config)
                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\.conda\meshgraphnets-main _modified\run_model.py", line 350, in learner
    trajectory = next(ds_iterator)
                 ^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\dataloader.py", line 633, in __next__
    data = self._next_data()
           ^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\dataloader.py", line 677, in _next_data
    data = self._dataset_fetcher.fetch(index)  # may raise StopIteration
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\_utils\fetch.py", line 32, in fetch
    data.append(next(self.dataset_iter))
                ^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\dataloader.py", line 633, in __next__
    data = self._next_data()
           ^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\dataloader.py", line 677, in _next_data
    data = self._dataset_fetcher.fetch(index)  # may raise StopIteration
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\_utils\fetch.py", line 54, in fetch
    return self.collate_fn(data)
           ^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\_utils\collate.py", line 265, in default_collate
    return collate(batch, collate_fn_map=default_collate_fn_map)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\utils\data\_utils\collate.py", line 150, in collate
    raise TypeError(default_collate_err_msg_format.format(elem_type))
TypeError: default_collate: batch must contain tensors, numpy arrays, numbers, dicts or lists; found <class 'torch_geometric.data.data.Data'>   
