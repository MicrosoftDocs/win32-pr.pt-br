---
title: Propriedade Pai IVMHardDisk (VPCCOMInterfaces.h)
description: Pai do disco rígido virtual diferencial.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propriedade pai Pc Virtual
- Propriedade pai Pc Virtual , interface IVMHardDisk
- INTERFACE IVMHardDisk PC Virtual, propriedade Pai
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0ba8d56ad09f7c8263e41b17d2e107a0a441408d22ffb604e95055c57fb21d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472096"
---
# <a name="ivmharddiskparent-property"></a>Propriedade IVMHardDisk::P arent

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o pai do disco rígido virtual diferencial.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a>Valor da propriedade

Define o [**objeto IVMHardDisk**](ivmharddisk.md) associado à imagem do disco rígido pai.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                                    | O parâmetro é **NULL.**<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                               | Esse não é um disco rígido diferencial, portanto, ele não tem pai.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | O sistema não pôde encontrar o arquivo de disco rígido virtual pai.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0X80070003</dt> </dl> | O sistema não pôde encontrar o caminho para o arquivo de disco rígido virtual pai.<br/>                                                                                                                                                                                                   |
| <dl> <dt>VM \_ O \_ E HD IMAGE OPEN FALHA \_ \_ \_ 0XA004067C</dt> <dt></dt> </dl>                  | Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.<br/>                                                                                                                                                                                               |
| <dl> <dt>VM \_ E \_ HD \_ IMAGE \_ ACCESS</dt> <dt>0xA0040681</dt> </dl>                      | Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.<br/>                                                                                                                                                                                             |
| <dl> <dt>VM \_ E \_ INCOMPATIBILIDADE \_ DE \_ ID \_ FILHO</dt> PAI <dt>0XA0040685</dt> </dl>            | A imagem de disco rígido virtual localizada pelo *parâmetro pai* não tem a mesma ID que a imagem de disco filho. Certifique-se de que a imagem  do disco rígido virtual pai localizada pelo parâmetro pai seja a mesma imagem usada para criar a imagem de disco rígido virtual diferencial.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

Essa propriedade só é válida com imagens de disco rígido diferenciais.

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

 

