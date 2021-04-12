---
title: Interface IVMTask (VPCCOMInterfaces. h)
description: Use a interface IVMTask para monitorar e controlar tarefas assíncronas para vários métodos COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Virtual PC de interface IVMTask
- Virtual PC de interface IVMTask, descrito
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e1d519471fe5b1fc32cb6365d1139243c85538
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499576"
---
# <a name="ivmtask-interface"></a>Interface IVMTask

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Use a interface **IVMTask** para monitorar e controlar tarefas assíncronas para vários métodos com.

## <a name="members"></a>Membros

A interface **IVMTask** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMTask** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMTask** tem esses métodos.



| Método                                                 | Descrição                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Cancelar**](ivmtask-cancel.md)                       | Cancela a tarefa.<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | Aguarda a conclusão da tarefa ou o intervalo de tempo limite especificado para decorrer.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMTask** tem essas propriedades.



| Propriedade                                                        | Tipo de acesso          | Descrição                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Descrição**](ivmtask-description.md)<br/>           | Somente leitura<br/> | Uma descrição da tarefa.<br/>                              |
| [**Erro**](ivmtask-error.md)<br/>                       | Somente leitura<br/> | O erro registrado para esta tarefa.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Somente leitura<br/> | A descrição de erro localizada registrada para esta tarefa.<br/> |
| [**ID**](ivmtask-id.md)<br/>                             | Somente leitura<br/> | Um identificador exclusivo para esta tarefa.<br/>                      |
| [**Iscancelável**](ivmtask-iscancelable.md)<br/>         | Somente leitura<br/> | Indica se a tarefa pode ser cancelada.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Somente leitura<br/> | Indica se a tarefa foi concluída.<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | Somente leitura<br/> | A porcentagem de conclusão da tarefa.<br/>                  |
| [**Resultado**](ivmtask-result.md)<br/>                     | Somente leitura<br/> | O resultado da tarefa.<br/>                                 |



 

## <a name="remarks"></a>Comentários

Um objeto **IVMTask** é retornado por métodos que potencialmente podem exigir uma quantidade significativa de tempo para serem concluídos. Isso permite que o aplicativo monitore o progresso da operação desejada sem forçá-la a bloquear a execução adicional enquanto aguarda a conclusão da operação.

Os métodos a seguir retornam um objeto **IVMTask** que pode ser usado para acompanhar o progresso:

-   [**IVMGuestOS:: fazer logoff**](ivmguestos-logoff.md)
-   [**IVMGuestOS:: reiniciar**](ivmguestos-restart.md)
-   [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk:: compactar**](ivmharddisk-compact.md)
-   [**IVMHardDisk:: Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk:: Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk:: Mergeto**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine:: Reset**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine:: salvar**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine:: Startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine:: Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine:: desativação**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



 

