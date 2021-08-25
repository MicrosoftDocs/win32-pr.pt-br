---
title: Propriedade ClearTextPassword IMsTscNonScriptable
description: Define a senha Área de Trabalho Remota ActiveX controle em formato de texto não criptografado.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota
- A propriedade ClearTextPassword Serviços de Área de Trabalho Remota , interface IMsTscNonScriptable
- Interface IMsTscNonScriptable Serviços de Área de Trabalho Remota , propriedade ClearTextPassword
- A propriedade ClearTextPassword Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable
- Interface IMsRdpClientNonScriptable Serviços de Área de Trabalho Remota , propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable2
- Interface IMsRdpClientNonScriptable2 Serviços de Área de Trabalho Remota , propriedade ClearTextPassword
- A propriedade ClearTextPassword Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable3
- Interface IMsRdpClientNonScriptable3 Serviços de Área de Trabalho Remota , propriedade ClearTextPassword
- A propriedade ClearTextPassword Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota , propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota , propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota objeto , MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota propriedade , ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota objeto , MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota propriedade , ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota objeto , MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota propriedade , ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota objeto , MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota propriedade , ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0519e7379eab529cc5275c85a11116764417d524a03dff2e1eab74a914b6560b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125046"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Propriedade IMsTscNonScriptable::ClearTextPassword

Define a senha Área de Trabalho Remota ActiveX controle em formato de texto não criptografado.

Essa propriedade é somente gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Valor da propriedade

A senha a ser usada para se conectar, especificada em formato de texto não criptografado.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK se** for bem-sucedido.

## <a name="remarks"></a>Comentários

A senha é passada para o servidor no canal de comunicação RDP criptografado com segurança. Depois que uma senha de texto não criptografado é definida, ela não pode ser recuperada em formato de texto não criptografado.

A **propriedade ClearTextPassword** só pode ser definida quando o Área de Trabalho Remota ActiveX controle não está no estado conectado. A configuração dessa propriedade falhará se o controle estiver conectado. Para verificar o estado conectado, recupere a [**propriedade IMsTscAx::Connected.**](imstscax-connected.md)

Você também pode chamar esse método para definir uma senha de texto não criptografado antes de convertê-la em uma senha codificada portátil ou em uma senha codificada binária (não portabilidade). Observe, no entanto, que as senhas codificadas não devem ser consideradas criptografadas com segurança.

Se você chamar esse método pela primeira vez para definir uma senha em formato de texto não criptografado, poderá converter a senha em formato codificado.

**Para converter uma senha de texto não criptografado em formato codificado**

1.  De definir a senha em formato de texto não criptografado na **propriedade ClearTextPassword.**
2.  Para recuperar a senha no formato codificado binário (não porportável), recupere a propriedade [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e as [**propriedades BinarySalt.**](imstscnonscriptable-binarysalt.md) A parte de senha codificada e a parte de sal são necessárias para definir uma senha no formato codificado binário.
3.  Para recuperar a senha no formato codificado portátil, recupere o [**método PortablePassword**](imstscnonscriptable-portablepassword.md) e as [**propriedades PortableSalt.**](imstscnonscriptable-portablesalt.md) Ambas as partes são necessárias para definir uma senha no formato codificado portátil.

Depois de seguir as três etapas anteriores, você pode definir a senha no formato codificado definindo as propriedades [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt**](imstscnonscriptable-binarysalt.md) ou [**PortablePassword**](imstscnonscriptable-portablepassword.md) e [**PortableSalt.**](imstscnonscriptable-portablesalt.md) Ambas as partes são necessárias.

Para habilitar o logon automático, você também deve definir as [**propriedades UserName**](imstscax-username.md) [**e Domain.**](imstscax-domain.md) Se a senha não autenticar o usuário, Windows caixa de diálogo Logon do usuário será exibida no servidor para solicitar a senha ao usuário.

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

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





