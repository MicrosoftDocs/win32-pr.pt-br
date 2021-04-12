---
title: Método IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Cria um arquivo de imagem de disquete.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- CreateFloppyDiskImage do método virtual PC
- Método CreateFloppyDiskImage Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método CreateFloppyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455624"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a>Método IVMVirtualPC:: CreateFloppyDiskImage

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Cria um arquivo de imagem de disquete.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*imagePath* \[ no\]
</dt> <dd>

O caminho completo para o novo arquivo de imagem de disco. A pasta que a contém será criada se não existir.

</dd> <dt>

*ImageType* \[ no\]
</dt> <dd>

O tipo de imagem de disquete a ser criado. Somente **vmFloppyDiskImage \_ LowDensity** (1) e **vmFloppyDiskImage \_ Highdensity** (2) têm suporte. Consulte [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                         | A operação foi bem-sucedida.<br/>                                                                                                                  |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro *imagePath* é **nulo**.<br/>                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O parâmetro *ImageType* não é [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) ou **vmFloppyDiskImage \_ Highdensity** (2).<br/> |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl> | O sistema não pode localizar o caminho especificado pelo parâmetro *imagePath* .<br/>                                                                        |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *imagePath* contém um caractere inválido (um de " \* ?: <>/ \| " ").<br/>                                                           |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *imagePath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                                                   |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelo parâmetro *imagePath* é muito longo. O comprimento do caminho deve ter menos de 260 caracteres.<br/>                          |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt> </dl>  | O arquivo referenciado pelo parâmetro *imagePath* já existe.<br/>                                                                               |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (disco de erro \_ \_ cheio)**</dt> <dt>0x80070070</dt> </dl>       | Não há espaço suficiente no volume do host para criar a imagem de disquete virtual.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Erro inesperado.<br/>                                                                                                                  |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl>     | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/>                                                           |



 

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

 

