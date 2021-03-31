---
title: Propriedade IMsTscNonScriptable ClearTextPassword
description: Define a Área de Trabalho Remota senha do controle ActiveX em formato de texto sem formatação.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsTscNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsTscNonScriptable, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
- Propriedade ClearTextPassword Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade ClearTextPassword
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
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645156"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Propriedade IMsTscNonScriptable:: ClearTextPassword

Define a Área de Trabalho Remota senha do controle ActiveX em formato de texto sem formatação.

Essa propriedade é somente gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Valor da propriedade

A senha a ser usada para conexão, especificada em formato de texto sem formatação.

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

A senha é passada para o servidor no canal de comunicações RDP criptografado com segurança. Depois que uma senha de texto sem formatação é definida, ela não pode ser recuperada no formato de texto sem formatação.

A propriedade **clearTextPassword** só pode ser definida quando o controle ActiveX área de trabalho remota não está no estado conectado. A definição dessa propriedade falhará se o controle estiver conectado. Para verificar o estado conectado, recupere a propriedade [**IMsTscAx:: Connected**](imstscax-connected.md) .

Você também pode chamar esse método para definir uma senha de texto sem formatação antes de convertê-la para uma senha codificada em portátil ou para uma senha codificada binária (não-Portable). No entanto, observe que as senhas codificadas não devem ser consideradas criptografadas com segurança.

Se você chamar primeiro este método para definir uma senha em formato de texto sem formatação, poderá converter a senha no formato codificado.

**Para converter uma senha de texto sem formatação em formato codificado**

1.  Defina a senha em formato de texto sem formatação na propriedade **clearTextPassword** .
2.  Para recuperar a senha em formato binário (não Portable) codificado, recupere a propriedade [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e as propriedades [**BinarySalt**](imstscnonscriptable-binarysalt.md) . A parte da senha codificada e a parte Salt são necessárias para definir uma senha no formato binário codificado.
3.  Para recuperar a senha no formato de codificação portátil, recupere o método [**PortablePassword**](imstscnonscriptable-portablepassword.md) e as propriedades [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Ambas as partes são necessárias para definir uma senha no formato codificado portátil.

Depois de seguir as três etapas anteriores, você pode definir a senha no formato codificado definindo as propriedades [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt**](imstscnonscriptable-binarysalt.md) ou as propriedades [**PortablePassword**](imstscnonscriptable-portablepassword.md) e [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Ambas as partes são necessárias.

Para habilitar o logon automático, você também deve definir as propriedades de [**nome de usuário**](imstscax-username.md) e [**domínio**](imstscax-domain.md) . Se a senha não autenticar o usuário, a caixa de diálogo logon do Windows será exibida no servidor para solicitar a senha ao usuário.

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

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





