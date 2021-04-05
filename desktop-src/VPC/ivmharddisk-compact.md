---
title: Método IVMHardDisk Compact (VPCCOMInterfaces. h)
description: Compacta uma imagem de disco rígido virtual de expansão dinâmica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- PC virtual do método compacto
- Método compacto Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, método compacto
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645086"
---
# <a name="ivmharddiskcompact-method"></a>Método IVMHardDisk:: Compact

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Compacta uma imagem de disco rígido virtual de expansão dinâmica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*compactTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a conclusão do processo de compactação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                              | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                    |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                      | O parâmetro é **NULL**.<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (violação de erro de \_ compartilhamento \_ )**</dt> <dt>0x80070020</dt> </dl> | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) está em uso.<br/>                                  |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt> </dl>         | O volume do host não tem espaço suficiente para criar um arquivo temporário necessário para a compactação desta imagem de disco rígido virtual.<br/>     |
| <dl> <dt>**VM \_ \_Aplicativo E \_ desligamento \_**</dt> do <dt>0xA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser compactada porque o aplicativo está sendo desligado.<br/>                                            |
| <dl> <dt>**VM \_ E \_ File \_ \_ somente leitura**</dt> <dt>0xA004067A</dt> </dl>                         | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) está marcada como somente leitura.<br/>                     |
| <dl> <dt>**VM \_ E \_ \_ tipo de \_ imagem \_ HD incorreto**</dt> <dt>0xA004067B</dt> </dl>                   | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) deve ser um tipo de imagem **vmDiskTypeDynamic** .<br/> |
| <dl> <dt>**VM \_ E \_ \_ \_ arquivo HD inválido**</dt> <dt>0xA0040682</dt> </dl>                        | A imagem do disco rígido virtual referenciada por este objeto [**IVMHardDisk**](ivmharddisk.md) não parece ser uma imagem válida.<br/>          |



 

## <a name="remarks"></a>Comentários

Para compactar uma imagem de disco rígido de expansão dinâmica, o espaço livre na imagem de disco deve ser zerado primeiro.

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

 

