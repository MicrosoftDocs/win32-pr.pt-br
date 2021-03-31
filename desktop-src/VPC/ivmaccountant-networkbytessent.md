---
title: Propriedade IVMAccountant NetworkBytesSent (VPCCOMInterfaces. h)
description: Número total de bytes enviados por todos os adaptadores de rede virtual para esta máquina virtual.
ms.assetid: 3b5c3fa2-48c6-46c8-bbb6-5d1a9769308a
keywords:
- Propriedade NetworkBytesSent Virtual PC
- Propriedade NetworkBytesSent Virtual PC, interface IVMAccountant
- IVMAccountant interface virtual PC, Propriedade NetworkBytesSent
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesSent
- IVMAccountant.get_NetworkBytesSent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d25a6c0a9ee784af8bfab196fc9aaef0d1474d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918543"
---
# <a name="ivmaccountantnetworkbytessent-property"></a>Propriedade IVMAccountant:: NetworkBytesSent

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número total de bytes enviados por todos os adaptadores de rede virtual para esta máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_NetworkBytesSent(
  [out, retval] VARIANT *bytesSent
);
```



## <a name="property-value"></a>Valor da propriedade

O número total de bytes enviados por todas as placas de interface de rede virtual para esta máquina virtual. Ele é retornado como uma **variante** do tipo **VT \_ decimal**.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>          |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                    | A máquina virtual não está em execução.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>   |



## <a name="remarks"></a>Comentários

Observe que as estatísticas de e/s de rede são redefinidas para zero quando uma máquina virtual é ligada, redefinida ou restaurada do estado salvo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

