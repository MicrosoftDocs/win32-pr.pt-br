---
title: Método IBackgroundCopyJob Complete (Deliveryoptimization.h)
description: Encerra o trabalho e salva os arquivos transferidos no cliente.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Método completo
- Método completo, interface IBackgroundCopyJob
- Interface IBackgroundCopyJob, método Complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72ace8890e724e529e96c5292a439042f13bc2bfad77e6d990a6dbb2fa18f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736211"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Método IBackgroundCopyJob::Complete

Encerra o trabalho e salva os arquivos transferidos no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT.** O método também pode retornar erros relacionados à renomeação das cópias temporárias dos arquivos transferidos para seus nomes determinados.



| Código de retorno                                                                                          | Descrição                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | Todos os arquivos transferidos com êxito.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Para downloads, o estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED. <br/> Para uploads, o estado do trabalho deve ser BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Comentários

Todos os arquivos foram transferidos com êxito se o estado do trabalho for **BG_JOB_STATE_TRANSFERRED**. Para verificar o estado do trabalho, chame o [**método IBackgroundCopyJob::GetState.**](ibackgroundcopyjob-getstate.md) Você também pode implementar a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para receber notificação quando todos os arquivos foram transferidos para o cliente.

O DO retém trabalhos com menos de 30 dias apenas. Todos os trabalhos mais antigos serão removidos. O DO não dá suporte à [função JobInactivityTimeout Política de Grupo.](https://www.bing.com/search?q=JobInactivityTimeout)

Para trabalhos de download, você pode chamar o **método Complete** a qualquer momento durante o processo de transferência; no entanto, somente os arquivos que foram transferidos com êxito para o cliente antes de chamar esse método são salvos. Por exemplo, se você chamar **o método Complete** enquanto DO estiver processando o terceiro de cinco arquivos, somente os dois primeiros arquivos serão salvos. Para determinar quais arquivos foram transferidos, chame o método [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) e compare o membro **BytesTransferred** com o membro **BytesTotal** da estrutura [**BG_FILE_PROGRESS.**](bg-file-progress.md)

Para trabalhos de upload, você pode chamar **o método Complete** somente quando o estado do trabalho for **BG_JOB_STATE_TRANSFERRED**.

O proprietário do arquivo é o usuário que fez a chamada. Por exemplo, se um administrador concluir o trabalho de outra pessoa, o administrador não o proprietário do trabalho será o proprietário do arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





