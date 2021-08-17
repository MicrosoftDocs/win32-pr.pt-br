---
title: Propriedade IMsRdpClient4 AdvancedSettings5
description: Recupera um ponteiro para uma interface IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Propriedades AdvancedSettings5 Serviços de Área de Trabalho Remota
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient4
- Interface IMsRdpClient4 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
- A propriedade AdvancedSettings5 Serviços de Área de Trabalho Remota , interface IMsRdpClient10
- Interface IMsRdpClient10 Serviços de Área de Trabalho Remota , propriedade AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb8efd8fae25be768a1b758389b5ca7c20a9f3f8b414e62acb865fecf83eeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138949"
---
# <a name="imsrdpclient4advancedsettings5-property"></a>Propriedade IMsRdpClient4::AdvancedSettings5

Recupera um ponteiro para uma interface [**IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para a interface [**IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md) A interface pode ser usada para definir configurações avançadas para o controle do cliente.

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem-sucedido, **S \_ OK** será retornado. Qualquer outro **valor HRESULT** indica que a chamada falhou.

## <a name="remarks"></a>Comentários

Essa propriedade não pode ser definida quando o controle está conectado.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for Conexão Web de Área de Trabalho Remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2008 com SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient4 é definido como 095E0738-D97D-488b-B9F6-DD0E8D66C0DE<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





