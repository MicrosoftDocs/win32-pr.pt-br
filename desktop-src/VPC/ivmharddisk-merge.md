---
title: Método IVMHardDisk Merge (VPCCOMInterfaces.h)
description: Mescla um disco rígido virtual diferencial com sua imagem de disco pai.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Computador Virtual do método merge
- Método de mesclagem PC virtual, interface IVMHardDisk
- INTERFACE IVMHardDisk pc virtual, método Merge
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
ms.openlocfilehash: 5b1683b5a44d8418dc247dddcfde52b369c293484e5c3b19c139fe25521ac6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998936"
---
# <a name="ivmharddiskmerge-method"></a>Método IVMHardDisk::Merge

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

Um [**objeto IVMTask**](ivmtask.md) usado para acompanhar a conclusão do processo de mesclamento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                              | Descrição                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                      | O parâmetro é **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0X80070020</dt> </dl> | A imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) está em uso ou o pai dessa imagem de disco rígido virtual está em uso. Ou essas imagens de disco rígido podem fazer parte de um estado salvo.<br/> |
| <dl> <dt>**VM \_ E \_ TIPO DE IMAGEM HD ERRADO \_ \_ \_ 0XA004067B**</dt> <dt></dt> </dl>                   | A imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) deve ser uma imagem de disco diferencial.<br/>                                                                                            |
| <dl> <dt>**VM \_ E \_ FILE READ ONLY \_ \_ 0XA004067A**</dt> <dt></dt> </dl>                         | O pai da imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) é marcado como somente leitura.<br/>                                                                                             |
| <dl> <dt>**VM \_ E \_ CAMINHO PAI NÃO ENCONTRADO \_ \_ \_ 0XA0040677**</dt> <dt></dt> </dl>                 | O pai do disco rígido virtual referenciado por este [**objeto IVMHardDisk**](ivmharddisk.md) não existe.<br/>                                                                                                       |
| <dl> <dt>**VM \_ E \_ O APLICATIVO ESTÁ \_ \_ DESLIGANDO**</dt> <dt>0XA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser mesclada porque o aplicativo está sendo desligado.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk é definido como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

