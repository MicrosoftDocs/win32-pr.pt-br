---
title: Propriedade IMsTscAx AdvancedSettings
description: Recupera um ponteiro de interface IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsTscAx
- Serviços de Área de Trabalho Remota de interface IMsTscAx, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient
- Serviços de Área de Trabalho Remota de interface IMsRdpClient, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings
- Propriedade AdvancedSettings Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918441"
---
# <a name="imstscaxadvancedsettings-property"></a>Propriedade IMsTscAx:: AdvancedSettings

Recupera um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .

## <a name="error-codes"></a>Códigos do Erro

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx é definido como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





