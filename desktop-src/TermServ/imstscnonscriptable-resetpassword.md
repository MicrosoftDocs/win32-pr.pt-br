---
title: Método ResetPassword IMsTscNonScriptable
description: Redefine todos os estados de senha no Área de Trabalho Remota ActiveX controle.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Método ResetPassword Serviços de Área de Trabalho Remota
- Método ResetPassword Serviços de Área de Trabalho Remota interface , IMsTscNonScriptable
- Interface IMsTscNonScriptable Serviços de Área de Trabalho Remota , método ResetPassword
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
ms.openlocfilehash: b039a66889dcbcab302223003d642dab71545772bb99db82d3ae40ae70cd3ff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118853570"
---
# <a name="imstscnonscriptableresetpassword-method"></a>Método IMsTscNonScriptable::ResetPassword

Redefine todos os estados de senha no Área de Trabalho Remota ActiveX controle. Você pode chamar esse método para limpar as senhas armazenadas em qualquer um dos três formatos com suporte: texto não criptografado, codificado portátil ou binário (não portável). Observe que as senhas codificadas não devem ser consideradas criptografadas com segurança.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

Você pode chamar esse método para redefinir a senha do controle após a desconexão. Isso garante que as conexões subsequentes que usam a mesma instância do controle não faça logoff automaticamente com uma senha definida anteriormente.

Você só pode chamar esse método quando o Área de Trabalho Remota ActiveX controle não está no estado conectado. Esse método **retornará E \_ FAIL** se for chamado quando o controle estiver conectado. Para verificar o estado conectado, chame o método [**get \_ Connected**](imstscax-connected.md) por meio da interface [**IMsTscAx**](imstscax-interface.md) ou uma das interfaces herdadas dele.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable é definido como c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





