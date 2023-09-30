# ModifiedMeshGraphNet

.pt data is in DATA/flag_simple_test
notebook used to create .pt data is in "data creation"

Model ran using this format
python -m run_model  --mode=train --model=cloth --dataset = DATA/flag_simple_test

After Running "runmodel.py" Should result in the following output and error

I0929 17:14:39.807608 294568 run_model.py:722] =========================================================
I0929 17:14:39.808604 294568 run_model.py:723] Start new run in C:\Users\trist\.conda\meshgraphnets-main _modified\output\=\Fri-Sep-29-17-14-39-2023\1
I0929 17:14:39.808604 294568 run_model.py:724] =========================================================
I0929 17:14:39.809574 294568 run_model.py:736] Program started at time Fri Sep 29 17:14:39 2023
I0929 17:14:39.809574 294568 run_model.py:740] Start training......
C:\Users\trist\anaconda3\Lib\site-packages\torch\nn\modules\lazy.py:180: UserWarning: Lazy modules are a new feature under heavy development so changes to the API or functionality can happen at any moment.
  warnings.warn('Lazy modules are a new feature under heavy development '
I0929 17:14:39.933243 294568 run_model.py:640] 
I0929 17:14:39.933243 294568 run_model.py:641] =======================Run Summary=======================
I0929 17:14:39.933243 294568 run_model.py:642] Simulation task is cloth simulation
I0929 17:14:39.933243 294568 run_model.py:643] Mode is train
I0929 17:14:39.933243 294568 run_model.py:647] No Evaluation
I0929 17:14:39.933243 294568 run_model.py:648] Train and/or evaluation configuration are 2 epochs, 2 trajectories each epoch, number of rollouts 
is 1
I0929 17:14:39.936235 294568 run_model.py:652] Core model is encode_process_decode
I0929 17:14:39.936235 294568 run_model.py:653] Message passing aggregator is sum
I0929 17:14:39.936235 294568 run_model.py:654] Message passing steps are 5
I0929 17:14:39.936235 294568 run_model.py:655] Attention used is False
I0929 17:14:39.936235 294568 run_model.py:656] Ripple used is False
I0929 17:14:39.937233 294568 run_model.py:665] Run output directory is C:\Users\trist\.conda\meshgraphnets-main _modified\output\=\Fri-Sep-29-17-14-39-2023\1
I0929 17:14:39.937233 294568 run_model.py:666] =========================================================
I0929 17:14:39.937233 294568 run_model.py:667]
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
  File "C:\Users\trist\.conda\meshgraphnets-main _modified\run_model.py", line 335, in learner
    ds_loader = dataset.load_dataset(run_step_config['dataset_dir'], 'train', batch_size=batch_size,
                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\.conda\meshgraphnets-main _modified\dataset.py", line 114, in load_dataset
    return DataLoader(FlagSimpleDatasetIterative(path=path, split=split, add_targets=add_targets, split_and_preprocess=split_and_preprocess), batch_size=batch_size, prefetch_factor=prefetch_factor, shuffle=False, num_workers=0)# , collate_fn=collate_fn)
                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^     
  File "C:\Users\trist\.conda\meshgraphnets-main _modified\migration_utilities\flag_simple_torch_dataset.py", line 28, in __init__
    pt_dataset = torch.load(pt_path)
                 ^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\serialization.py", line 791, in load
    with _open_file_like(f, 'rb') as opened_file:
         ^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\serialization.py", line 271, in _open_file_like
    return _open_file(name_or_buffer, mode)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\trist\anaconda3\Lib\site-packages\torch\serialization.py", line 252, in __init__
    super().__init__(open(name, mode))
                     ^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: 'data\\=\\train.pt'
