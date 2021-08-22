---
title: Propriedade do tipo IVMHardDisk (VPCCOMInterfaces. h)
description: Tipo de disco rígido virtual.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Propriedade de tipo Virtual PC
- Propriedade de tipo Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade Type
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c2ba462496f6791d129918b93401c971b755ef40c40ef9a1177059dc7bcce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998926"
---
# <a name="ivmharddisktype-property"></a>Propriedade IVMHardDisk:: Type

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o tipo de disco rígido virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Valor da propriedade

O tipo da imagem do disco rígido atual.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                  |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro é **NULL**.<br/>                                                     |
| <dl> <dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt> </dl> | Não foi possível encontrar o arquivo de imagem de disco rígido atual.<br/>                           |
| <dl> <dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt> </dl>                         | O tipo da imagem do disco rígido atual é inválido.<br/>                            |
| <dl> <dt>VM \_ 0xA004067C \_ de \_ \_ \_ falha de abertura de imagem de HD</dt> <dt></dt> </dl>                  | Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.<br/>   |
| <dl> <dt>VM \_ E & 0xA0040681 de \_ \_ \_ acesso de imagem de HD</dt> <dt></dt> </dl>                      | Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

