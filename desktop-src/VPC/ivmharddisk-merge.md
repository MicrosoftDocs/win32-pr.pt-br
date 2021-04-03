---
title: Método de mesclagem IVMHardDisk (VPCCOMInterfaces. h)
description: Mescla um disco rígido virtual diferencial com sua imagem de disco pai.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Método de mesclagem Virtual PC
- Método de mesclagem Virtual PC, interface IVMHardDisk
- Virtual PC de interface IVMHardDisk, método Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918643"
---
# <a name="ivmharddiskmerge-method"></a>Método IVMHardDisk:: Merge

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Mescla um disco rígido virtual diferencial com sua imagem de disco pai.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de mesclagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                              | Descrição                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                      | O parâmetro é **NULL**.<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt> </dl> | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) está em uso ou o pai desta imagem de disco rígido virtual está em uso. Ou, essas imagens de disco rígido podem fazer parte de um estado salvo.<br/> |
| <dl> <dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt> </dl>                   | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) deve ser uma imagem de disco diferencial.<br/>                                                                                            |
| <dl> <dt>**VM \_ E \_ File \_ \_ somente leitura**</dt> <dt>0xA004067A</dt> </dl>                         | O pai da imagem do disco rígido virtual referenciado por este objeto [**IVMHardDisk**](ivmharddisk.md) está marcado como somente leitura.<br/>                                                                                             |
| <dl> <dt>**VM \_ E \_ \_ caminho pai \_ não \_ encontrado**</dt> <dt>0xA0040677</dt> </dl>                 | O pai do disco rígido virtual referenciado por este objeto [**IVMHardDisk**](ivmharddisk.md) não existe.<br/>                                                                                                       |
| <dl> <dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser mesclada porque o aplicativo está sendo desligado.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                      |



 

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

 

