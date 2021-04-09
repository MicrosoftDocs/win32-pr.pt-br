---
title: Propriedade IVMHardDisk SizeOnHost (VPCCOMInterfaces. h)
description: Tamanho do arquivo de disco rígido virtual no computador host.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Propriedade SizeOnHost Virtual PC
- Propriedade SizeOnHost Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009579"
---
# <a name="ivmharddisksizeonhost-property"></a>Propriedade IVMHardDisk:: SizeOnHost

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o tamanho do arquivo de disco rígido virtual no computador host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valor da propriedade

O tamanho, em bytes, do arquivo de imagem de disco rígido. Esse valor é uma **variante** do tipo **VT \_ decimal**.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>           |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro é **NULL**.<br/>              |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>       |
| <dl> <dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt> </dl> | O arquivo de imagem do disco rígido não foi encontrado.<br/> |



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

 

