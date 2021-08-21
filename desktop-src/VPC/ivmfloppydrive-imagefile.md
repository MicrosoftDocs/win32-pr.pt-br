---
title: Propriedade ImageFile de IVMFloppyDrive (VPCCOMInterfaces. h)
description: Recupera o caminho completo do arquivo de imagem ao qual a unidade de disquete está anexada.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- Propriedade ImageFile Virtual PC
- Propriedade ImageFile Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive da interface virtual PC, propriedade ImageFile
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44c76498d192954dde50e3f997fe91ce405344fc2048697ce996723aa0e6d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595116"
---
# <a name="ivmfloppydriveimagefile-property"></a>Propriedade IVMFloppyDrive:: ImageFile

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o caminho completo do arquivo de imagem ao qual a unidade de disquete está anexada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a>Valor da propriedade

O caminho completo do arquivo de imagem.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                               |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                                                  |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração desta máquina virtual não é válida ou não foi encontrada.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

