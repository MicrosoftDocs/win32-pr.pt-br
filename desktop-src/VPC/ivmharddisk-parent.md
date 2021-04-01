---
title: Propriedade pai IVMHardDisk (VPCCOMInterfaces. h)
description: Pai do disco rígido virtual diferencial.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propriedade pai Virtual PC
- Propriedade pai Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade Parent
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
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917956"
---
# <a name="ivmharddiskparent-property"></a>IVMHardDisk: Propriedade porcentagem de:P

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o pai do disco rígido virtual diferencial.

Esta propriedade é de leitura/gravação.

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

Define o objeto [**IVMHardDisk**](ivmharddisk.md) associado à imagem do disco rígido pai.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                                                              |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro é **NULL**.<br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                               | Esse não é um disco rígido diferencial, portanto, ele não tem nenhum pai.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt> </dl> | O sistema não pôde localizar o arquivo de disco rígido virtual pai.<br/>                                                                                                                                                                                                               |
| <dl> <dt>HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070003</dt> </dl> | O sistema não pôde localizar o caminho para o arquivo de disco rígido virtual pai.<br/>                                                                                                                                                                                                   |
| <dl> <dt>VM \_ 0xA004067C \_ de \_ \_ \_ falha de abertura de imagem de HD</dt> <dt></dt> </dl>                  | Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.<br/>                                                                                                                                                                                               |
| <dl> <dt>VM \_ E & 0xA0040681 de \_ \_ \_ acesso de imagem de HD</dt> <dt></dt> </dl>                      | Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.<br/>                                                                                                                                                                                             |
| <dl> <dt>VM \_ Não \_ há \_ \_ \_ incompatibilidade de ID de filho pai do E</dt> <dt>0xA0040685</dt> </dl>            | A imagem do disco rígido virtual localizado pelo parâmetro *pai* não tem a mesma ID da imagem do disco filho. Verifique se a imagem do disco rígido virtual pai localizado pelo parâmetro *pai* é a mesma imagem usada para criar a imagem de disco rígido virtual diferencial.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

Essa propriedade só é válida com imagens de disco rígido diferencial.

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

 

