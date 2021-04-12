---
title: Propriedade IMsRdpClient2 AdvancedSettings3
description: Recupera um ponteiro para a interface IMsRdpClientAdvancedSettings2. A interface pode ser usada para definir configurações avançadas para o controle de cliente.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient2
- Serviços de Área de Trabalho Remota de interface IMsRdpClient2, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient3
- Serviços de Área de Trabalho Remota de interface IMsRdpClient3, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient4
- Serviços de Área de Trabalho Remota de interface IMsRdpClient4, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, Propriedade AdvancedSettings3
- Propriedade AdvancedSettings3 Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, Propriedade AdvancedSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295811"
---
# <a name="imsrdpclient2advancedsettings3-property"></a>Propriedade IMsRdpClient2:: AdvancedSettings3

Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . A interface pode ser usada para definir configurações avançadas para o controle de cliente.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a>Valor da propriedade

Recupera um ponteiro para a interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem sucedido, **S \_ OK** será retornado. Qualquer outro valor **HRESULT** indica que a chamada falhou.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient2 é definido como e7e17dc4-3b71-4ba7-a8e6-281ffadca28f<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





