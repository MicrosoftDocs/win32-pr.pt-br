---
title: Método IMsTscNonScriptable ResetPassword
description: Redefine todos os Estados de senha no controle ActiveX Área de Trabalho Remota.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ResetPassword
- Método ResetPassword Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, método ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455868"
---
# <a name="imstscnonscriptableresetpassword-method"></a>Método IMsTscNonScriptable:: ResetPassword

Redefine todos os Estados de senha no controle ActiveX Área de Trabalho Remota. Você pode chamar esse método para limpar as senhas que são armazenadas em qualquer um dos três formatos com suporte: texto não criptografado, codificado em Portable ou binário (não Portable). Observe que as senhas codificadas não devem ser consideradas criptografadas com segurança.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Você pode chamar esse método para redefinir a senha do controle após a desconexão. Isso garante que as conexões subsequentes que usam a mesma instância do controle não façam logon automaticamente com uma senha definida anteriormente.

Você só pode chamar esse método quando o controle ActiveX Área de Trabalho Remota não está no estado conectado. Esse método retorna **E \_ falha** se chamado quando o controle está conectado. Para verificar o estado conectado, chame o método [**Get \_ conectado**](imstscax-connected.md) por meio da interface [**IMsTscAx**](imstscax-interface.md) ou uma das interfaces herdadas dele.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





