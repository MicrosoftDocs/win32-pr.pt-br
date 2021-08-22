---
title: Propriedade AuthenticationType IMsRdpClientAdvancedSettings6
description: Especifica o tipo de autenticação usado para essa conexão.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Propriedade AuthenticationType Serviços de Área de Trabalho Remota
- A propriedade AuthenticationType Serviços de Área de Trabalho Remota interface , IMsRdpClientAdvancedSettings6
- Interface IMsRdpClientAdvancedSettings6 Serviços de Área de Trabalho Remota , propriedade AuthenticationType
- A propriedade AuthenticationType Serviços de Área de Trabalho Remota interface , IMsRdpClientAdvancedSettings7
- Interface IMsRdpClientAdvancedSettings7 Serviços de Área de Trabalho Remota , propriedade AuthenticationType
- A propriedade AuthenticationType Serviços de Área de Trabalho Remota interface , IMsRdpClientAdvancedSettings8
- Interface IMsRdpClientAdvancedSettings8 Serviços de Área de Trabalho Remota , propriedade AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f35fe580ce780a51c3a203ff22b4043bbbe423dc4e821de1aaa2ba378485e719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138839"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a>Propriedade IMsRdpClientAdvancedSettings6::AuthenticationType

Especifica o tipo de autenticação usado para essa conexão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a>Valor da propriedade

Recebe um valor que especifica o tipo de autenticação usado para essa conexão. Esse pode ser um dos valores a seguir.

<dt>

0
</dt> <dd>

Nenhuma autenticação é usada.

</dd> <dt>

1
</dt> <dd>

A autenticação de certificado é usada.

</dd> <dt>

2
</dt> <dd>

A autenticação Kerberos é usada.

</dd> <dt>

3
</dt> <dd>

Tanto o certificado quanto a autenticação Kerberos são usados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | \_IMs IIDRdpClientAdvancedSettings6 é definido como 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





