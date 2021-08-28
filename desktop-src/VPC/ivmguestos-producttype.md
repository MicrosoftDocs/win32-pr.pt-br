---
title: Propriedade ProductType IVMGuestOS (VPCCOMInterfaces.h)
description: Recupera o tipo de produto do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Propriedade ProductType Pc Virtual
- Propriedade ProductType Pc Virtual , interface IVMGuestOS
- INTERFACE IVMGuestOS PC Virtual, propriedade ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c31b3b91cf75687d82e02e3b97c78dd0e40f724756b609a3e2b60c73812ee5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512306"
---
# <a name="ivmguestosproducttype-property"></a>Propriedade IVMGuestOS::P roductType

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o tipo de produto do sistema operacional convidado em execução na máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a>Valor da propriedade

O tipo de produto. Há suporte para os valores de cadeia de caracteres a seguir.



| Valor                                                                                  | Significado                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x0000002"</dt> </dl> | O sistema é um controlador de domínio e o sistema operacional é Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | O sistema operacional é Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 ou Windows 2000 Server.<br/> Observe que um servidor que também é um controlador de domínio é relatado como **VER \_ NT \_ DOMAIN \_ CONTROLLER,** não **VER \_ NT \_ SERVER.**<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | O sistema operacional é Windows 7, Windows Vista, Windows XP ou Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

