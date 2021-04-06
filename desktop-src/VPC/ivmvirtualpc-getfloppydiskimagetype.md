---
title: Método IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Recupera o tipo de um arquivo de imagem de disquete existente.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- GetFloppyDiskImageType do método virtual PC
- Método GetFloppyDiskImageType Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086343"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a>Método IVMVirtualPC:: GetFloppyDiskImageType

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o tipo de um arquivo de imagem de disquete existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*imagePath* \[ no\]
</dt> <dd>

O caminho completo para o arquivo de imagem de disco.

</dd> <dt>

*ImageType* \[ out, retval\]
</dt> <dd>

O tipo de imagem de disco. Para obter uma lista de valores, consulte [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                         |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro *imagePath* ou *ImageType* é **nulo**.<br/>                                                                 |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt> </dl> | O sistema não pode localizar o arquivo especificado pelo parâmetro *imagePath* .<br/>                                               |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl> | O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .<br/>                                               |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").<br/>                                  |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *imagePath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                          |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelo parâmetro *imagePath* é muito longo. O comprimento do caminho deve ter menos de 260 caracteres.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | O arquivo especificado por *imagePath* não é uma imagem de disquete ou ocorreu um erro inesperado.<br/>                         |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl>     | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/>                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

