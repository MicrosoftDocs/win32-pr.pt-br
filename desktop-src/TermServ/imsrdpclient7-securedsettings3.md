---
title: Propriedade IMsRdpClient7 SecuredSettings3
description: Recupera um objeto que dá suporte à interface IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , propriedade SecuredSettings3
- Propriedade SecuredSettings3 Serviços de Área de Trabalho Remota , interface IMsRdpClient10
- Interface IMsRdpClient10 Serviços de Área de Trabalho Remota , propriedade SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77bcdaae672ca59c65bea46d97a34046c7e48c6f0964c1a5b97cdcef77c14ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737166"
---
# <a name="imsrdpclient7securedsettings3-property"></a>Propriedade IMsRdpClient7::SecuredSettings3

Recupera um objeto que dá suporte à interface [**IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço de um ponteiro de interface [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) que recebe o objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444a-91d4-add26d070638<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





