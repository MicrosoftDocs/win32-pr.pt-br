---
title: Método IMsTscAxEvents OnConfirmClose
description: Chamado quando o cliente chama o método IMsRdpClient RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnConfirmClose
- Método OnConfirmClose Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086491"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>Método IMsTscAxEvents:: OnConfirmClose

Chamado quando o cliente chama o método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) . Em resposta a esse evento, o usuário deve ser solicitado a confirmar o fechamento da conexão. Para obter mais informações, consulte a seção Comentários a seguir.

## <a name="syntax"></a>Sintaxe


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pfAllowClose* \[ fora\]
</dt> <dd>

Se **Variant \_ true**, o padrão, indica que o usuário deseja fechar a conexão. Se **Variant \_ false**, indica que o usuário não deseja fechar a conexão. Para obter mais informações, consulte a seção Comentários a seguir.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando um aplicativo de contêiner chama o método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) , esse método retorna um valor que indica se o contêiner deve aguardar a ocorrência de um evento **OnConfirmClose** antes de fechar a conexão de controle. Se **RequestClose** retornar **controlCloseWaitForEvents** e o usuário estiver conectado e conectado à sua sessão de serviços de área de trabalho remota, o evento **OnConfirmClose** será acionado. Nesse ponto, o aplicativo de contêiner pode solicitar o usuário, perguntando se o usuário deseja fechar a conexão. Se o usuário quiser fechar a conexão, o aplicativo deverá definir o parâmetro *pfAllowClose* como **Variant \_ true** e continuar com o fechamento da conexão. Se o usuário não quiser fechar, o aplicativo deverá definir *pfAllowClose* como **Variant \_ false** e deixar a conexão aberta.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





