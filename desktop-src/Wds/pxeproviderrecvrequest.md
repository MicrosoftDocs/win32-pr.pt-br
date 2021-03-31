---
title: Função de retorno de chamada PxeProviderRecvRequest
description: Chamado quando uma solicitação é recebida de um cliente.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Função de retorno de chamada do PxeProviderRecvRequest serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369619"
---
# <a name="pxeproviderrecvrequest-callback-function"></a>Função de retorno de chamada PxeProviderRecvRequest

Chamado quando uma solicitação é recebida de um cliente. Essa função é registrada chamando a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o parâmetro *CallbackType* definido como **\_ \_ \_ solicitação de recepção de retorno de chamada PXE**.

## <a name="syntax"></a>Sintaxe


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hClientRequest* \[ no\]
</dt> <dd>

Identificador para uma solicitação recebida de um cliente.

</dd> <dt>

*pPacket* \[ no\]
</dt> <dd>

Ponteiro para o buffer de memória que contém o pacote recebido.

</dd> <dt>

*uPacketLen* \[ no\]
</dt> <dd>

Comprimento, em bytes, do buffer apontado pelo parâmetro *pPacket* .

</dd> <dt>

*pLocalAddress* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ endereço PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contém o endereço local no qual o pacote foi recebido.

</dd> <dt>

*pRemoteAddress* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ endereço PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) que contém o endereço de origem do pacote.

</dd> <dt>

*pAction* \[ fora\]
</dt> <dd>

Especifica a ação que o sistema deve executar.



| Valor                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt> </dl>                | O provedor respondeu a um cliente com um pacote de resposta DHCP padrão que contém um caminho para o programa de inicialização de rede. Retornar essa ação significa que o provedor concluiu com êxito a solicitação do cliente chamando a função [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) pelo menos uma vez.<br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <dt>**PXE \_ BA \_ personalizada**</dt> <dt>2</dt> </dl>       | O provedor respondeu a um cliente usando uma resposta personalizada que não está em conformidade com as especificações de DHCP. Retornar essa ação significa que o provedor concluiu com êxito a solicitação do cliente chamando a função [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) pelo menos uma vez.<br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <dt>**PXE \_ BA \_ ignorar**</dt> <dt>3</dt> </dl>       | O provedor não deseja atender à solicitação do cliente e a solicitação não deve ser passada para o próximo provedor. Todos os recursos associados à solicitação do cliente são liberados e a solicitação do cliente é ignorada. Os provedores também podem usar esse valor se reconhecerem o cliente, mas a solicitação tiver sido malformada.<br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <dt>**PXE \_ BA \_ rejeitada**</dt> <dt>4</dt> </dl> | O provedor não deseja atender à solicitação do cliente. O sistema passa a solicitação para o próximo provedor na lista de provedores registrados. Se esse for o último provedor na lista, todos os recursos associados à solicitação do cliente serão liberados e a solicitação do cliente será ignorada.<br/>                     |



 

</dd> <dt>

*pContext* \[ no\]
</dt> <dd>

Valor de contexto passado para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o provedor tiver processado com êxito a solicitação do cliente, o retorno de chamada deverá retornar o **\_ êxito do erro** e a **\_ \_ ação de inicialização PXE** apontada pelo parâmetro *pAction* conterá a ação de inicialização apropriada para essa solicitação. Se o provedor processar a solicitação do cliente de forma assíncrona, o retorno de chamada deverá retornar o **erro e \_ /s \_ pendente** e chamar a função [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) quando a solicitação do cliente tiver sido processada. Em caso de falha, um código de erro apropriado deve ser retornado e o sistema continuará como se a ação de inicialização de **BA do PXE \_ \_ rejeitada** fosse especificada.

## <a name="remarks"></a>Comentários

O tipo de pacotes visto por um provedor pode ser alterado com a função [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de servidor dos serviços de implantação do Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





