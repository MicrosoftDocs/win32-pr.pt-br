---
title: Propriedade ProductType IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera o tipo de produto do sistema operacional convidado em execução na máquina virtual.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Propriedade ProductType Virtual PC
- Propriedade ProductType Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, propriedade ProductType
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
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759587"
---
# <a name="ivmguestosproducttype-property"></a>IVMGuestOS: Propriedade roductType de:P

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>"0x0000002"</dt> </dl> | O sistema é um controlador de domínio e o sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | O sistema operacional é o Windows Server 2008 R2, o Windows Server 2008, o Windows Server 2003 R2, o Windows Server 2003 ou o Windows 2000 Server.<br/> Observe que um servidor que também é um controlador de domínio é relatado **como \_ \_ \_ controlador de domínio do NT**, não ver o **\_ \_ servidor NT**.<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | O sistema operacional é o Windows 7, o Windows Vista, o Windows XP ou o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

