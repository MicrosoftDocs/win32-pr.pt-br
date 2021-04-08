---
title: Propriedade IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces. h)
description: Recupera a quantidade de espaço em disco restante disponível no host para o disco rígido virtual.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Propriedade HostFreeDiskSpace Virtual PC
- Propriedade HostFreeDiskSpace Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086266"
---
# <a name="ivmharddiskhostfreediskspace-property"></a>Propriedade IVMHardDisk:: HostFreeDiskSpace

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a quantidade de espaço em disco restante disponível no host para o disco rígido virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a>Valor da propriedade

A quantidade de espaço em disco restante disponível no computador host para o arquivo de imagem de disco rígido atual. Esse valor é uma **variante** do tipo VT \_ decimal.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                            | Significado                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                               | A operação foi bem-sucedida.<br/>                                |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                 | O parâmetro é **NULL**.<br/>                                   |
| <dl> <dt>HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)</dt> <dt>0x800700a1</dt> </dl> | O caminho para o arquivo de disco rígido virtual atual não é válido.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                         | Ocorreu um erro inesperado.<br/>                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

