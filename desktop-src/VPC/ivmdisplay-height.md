---
title: Propriedade IVMDisplay Height (VPCCOMInterfaces. h)
description: Altura da exibição da máquina virtual, em pixels.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Propriedade de altura Virtual PC
- Propriedade Height Virtual PC, interface IVMDisplay
- IVMDisplay da interface virtual PC, Propriedade Height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009440"
---
# <a name="ivmdisplayheight-property"></a>Propriedade IVMDisplay:: Height

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a altura da exibição da máquina virtual, em pixels.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a>Valor da propriedade

A altura, em pixels.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>                                 |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro é **NULL**.<br/>                                    |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl> | A máquina virtual deve estar em execução para esta operação.<br/>       |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>      | A máquina virtual não é válida ou não está em execução no momento.<br/> |
| <dl> <dt>VM \_ E \_ nenhum \_ </dt> <dt>0xA0040850</dt> de exibição </dl>      | Não é possível localizar uma exibição válida para a máquina virtual.<br/>     |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

