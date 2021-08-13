---
title: Método IVMHardDisk Compact (VPCCOMInterfaces.h)
description: Compacta uma imagem de disco rígido virtual em expansão dinâmica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Compact method Virtual PC
- Compact method Virtual PC , IVMHardDisk interface
- INTERFACE IVMHardDisk Pc Virtual , método Compact
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
ms.openlocfilehash: 9d2ae6c8bcb4237f98c8bcb47089294b202e3e9c45e51351c9818a08e2a295ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472156"
---
# <a name="ivmharddiskcompact-method"></a>Método IVMHardDisk::Compact

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Compacta uma imagem de disco rígido virtual em expansão dinâmica.

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

Um [**objeto IVMTask**](ivmtask.md) usado para acompanhar a conclusão do processo de compactação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                              | Descrição                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | A operação foi bem-sucedida.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ocorreu um erro inesperado.<br/>                                                                                                    |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                      | O parâmetro é **NULL.**<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0X80070020</dt> </dl> | A imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) está em uso.<br/>                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | O volume do host não tem espaço suficiente para criar um arquivo temporário necessário para a compactação dessa imagem de disco rígido virtual.<br/>     |
| <dl> <dt>**VM \_ E \_ O APLICATIVO ESTÁ \_ \_ DESLIGANDO**</dt> <dt>0XA0040209</dt> </dl>                      | A imagem do disco rígido virtual não pode ser compactada porque o aplicativo está sendo desligado.<br/>                                            |
| <dl> <dt>**VM \_ SOMENTE \_ LEITURA \_ DE \_ ARQUIVO E**</dt> <dt>0XA004067A</dt> </dl>                         | A imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) é marcada como somente leitura.<br/>                     |
| <dl> <dt>**VM \_ E \_ TIPO DE IMAGEM HD ERRADO \_ \_ \_ 0XA004067B**</dt> <dt></dt> </dl>                   | A imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) deve ser um tipo de imagem **vmDiskTypeDynamic.**<br/> |
| <dl> <dt>**VM \_ E \_ ARQUIVO HD INVÁLIDO \_ \_ 0XA0040682**</dt> <dt></dt> </dl>                        | A imagem de disco rígido virtual referenciada por este [**objeto IVMHardDisk**](ivmharddisk.md) não parece ser uma imagem válida.<br/>          |



 

## <a name="remarks"></a>Comentários

Para compactar uma imagem de disco rígido de expansão dinâmica, o espaço livre na imagem de disco deve primeiro ser zerado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk é definido como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

