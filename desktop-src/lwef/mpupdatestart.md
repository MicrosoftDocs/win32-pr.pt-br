---
title: Função MpUpdateStart (MpClient. h)
description: Inicia uma operação de atualização de assinatura.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- recursos de ambiente de Windows herdado da função MpUpdateStart
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61cda213ecfbb23c9ef366fcce7b5c91e806f26f0f4ebe8b45dc596b63d1b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975886"
---
# <a name="mpupdatestart-function"></a>Função MpUpdateStart

Inicia uma operação de atualização de assinatura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*dwUpdateOptions* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Especifica a opção para a operação de atualização de assinatura. Pode ser um dos seguintes valores:



| Valor                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**\_opção MPUPDATE \_ None**</dt> </dl>                | Nenhuma opção específica é solicitada.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**\_opção MPUPDATE \_ Async**</dt> </dl>             | A operação de atualização deve ser assíncrona, em que **MpUpdateStart** retorna imediatamente após o início bem-sucedido da atualização de assinatura. (Por padrão, a operação de atualização é síncrona, o que significa que **MpUpdateStart** retornará somente depois que a atualização da assinatura for concluída.)<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**\_progresso da opção MPUPDATE \_**</dt> </dl>    | O chamador está interessado em receber informações de progresso de atualização de assinatura por meio de um retorno de chamada.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**\_opção MPUPDATE \_ http**</dt> </dl>                | A atualização de assinatura é executada baixando o pacote de assinatura completo do site do portal de segurança da Microsoft. Isso pode ser usado como uma opção de fallback se o cliente estiver enfrentando um problema de download de assinatura por meio de Microsoft Update.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**\_UNC de opção MPUPDATE \_**</dt> </dl>                   | Executa a atualização de assinatura usando download direto de compartilhamentos UNC.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**\_opção MPUPDATE \_ gerenciada**</dt> </dl>       | Executa a atualização de assinatura usando o WSUS do serviço gerenciado.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**\_opção MPUPDATE \_ não gerenciada**</dt> </dl> | Executa a atualização de assinatura usando o serviço não gerenciado MU/WU.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ em, opcional\]
</dt> <dd>

Tipo: **\_ informações de PMPCALLBACK**

Um ponteiro para as informações de retorno de chamada usadas para alimentar o cliente com alterações de estado de atualização de assinatura (como iniciar e concluir) e informações de progresso. Os [**\_ dados de MPCALLBACK**](mpcallback-data.md) passados na função de retorno de chamada relatam o estado de atualização real e informações relacionadas ao progresso. Veja a seguir uma lista de possíveis retornos de chamada:



| Valor                                                                                                                                                                                                                                | Significado                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ Start**</dt> </dl>                                      | Operação de atualização iniciada.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ concluída**</dt> </dl>                             | Operação de atualização concluída.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**início da pesquisa do MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>                | Pesquisa de atualizações iniciada.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**pesquisa do MPNOTIFY \_ SIGUPDATE \_ \_ concluída**</dt> </dl>       | Pesquisa de atualizações concluída. Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**início do download do MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>          | Download para a atualização iniciado.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**progresso do download do MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl> | Baixar informações de progresso. Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**Download do MPNOTIFY \_ SIGUPDATE \_ \_ concluído**</dt> </dl> | Download para atualização concluído. Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**início da instalação do MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>             | Instalação da atualização iniciada.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**progresso da instalação do MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>    | Informações de progresso da instalação. Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**instalação do MPNOTIFY \_ SIGUPDATE \_ \_ concluída**</dt> </dl>    | Instalação da atualização concluída. Informações adicionais estão disponíveis por meio da estrutura de [**\_ dados MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**\_solicitação mpnotify \_ SIGUPDATE \_ processada**</dt> </dl> | O serviço Antimalware processou uma solicitação de atualização de assinatura. A falha ou o êxito é indicado por *HRESULT* nos [**\_ dados de MPCALLBACK**](mpcallback-data.md).<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**\_reinicialização mpnotify SIGUPDATE \_ \_ necessária**</dt> </dl>       | Requer reinicialização para concluir a operação de atualização. A falha ou o êxito é indicado por *HRESULT* nos [**\_ dados de MPCALLBACK**](mpcallback-data.md).<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_falha interna do mpnotify \_**</dt> </dl>                                   | A operação de atualização de assinatura encontrou uma falha genérica. O *HRESULT* nos [**\_ dados MPCALLBACK**](mpcallback-data.md) tem o código de erro específico.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ fora\]
</dt> <dd>

Tipo: **PMPHANDLE**

O identificador de atualização retornado que identifica a operação de atualização de assinatura iniciada no momento. Esse identificador pode ser usado em chamadas de função subsequentes, como para controlar a operação de atualização de assinatura. O identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**dados do MPCALLBACK \_**](mpcallback-data.md)
</dt> <dt>

[**DADOS MPSIGUPDATE \_**](mpsigupdate-data.md)
</dt> </dl>

 

 





