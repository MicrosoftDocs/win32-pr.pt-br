---
title: Método Complete método ibackgroundcopyjob (Deliveryoptimization. h)
description: Encerra o trabalho e salva os arquivos transferidos no cliente.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Método Complete
- Método Complete, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método Complete
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
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085548"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Método método ibackgroundcopyjob:: Complete

Encerra o trabalho e salva os arquivos transferidos no cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores de **HRESULT** a seguir. O método também pode retornar erros relacionados à renomeação das cópias temporárias dos arquivos transferidos para seus nomes especificados.



| Código de retorno                                                                                          | Descrição                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Todos os arquivos foram transferidos com êxito.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Para downloads, o estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED. <br/> Para carregamentos, o estado do trabalho deve ser BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Comentários

Todos os arquivos foram transferidos com êxito se o estado do trabalho for **BG_JOB_STATE_TRANSFERRED**. Para verificar o estado do trabalho, chame o método [**método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) . Você também pode implementar a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para receber notificações quando todos os arquivos tiverem sido transferidos para o cliente.

O retém trabalhos com menos de 30 dias. Todos os trabalhos mais antigos serão removidos. O não oferece suporte ao Política de Grupo [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) .

Para baixar trabalhos, você pode chamar o método **Complete** a qualquer momento durante o processo de transferência; no entanto, somente os arquivos que foram transferidos com êxito para o cliente antes de chamar esse método são salvos. Por exemplo, se você chamar o método **Complete** enquanto o estiver processando o terceiro dos cinco arquivos, somente os dois primeiros arquivos serão salvos. Para determinar quais arquivos foram transferidos, chame o método [**IBackgroundCopyFile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md) e compare o membro **bytesTransferred** com o membro **bytesTotal** da estrutura [**BG_FILE_PROGRESS**](bg-file-progress.md) .

Para trabalhos de carregamento, você pode chamar o método **Complete** somente quando o estado do trabalho for **BG_JOB_STATE_TRANSFERRED**.

O proprietário do arquivo é o usuário que fez a chamada. Por exemplo, se um administrador concluir o trabalho de outra pessoa, o administrador não o proprietário do trabalho possui o arquivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





