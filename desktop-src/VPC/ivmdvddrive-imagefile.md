---
title: Propriedade ImageFile IVMDVDDrive (VPCCOMInterfaces.h)
description: Recupera o caminho completo do conjunto de arquivos de imagem para este dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Propriedade ImageFile Pc Virtual
- Propriedade ImageFile Pc Virtual , interface IVMDVDDrive
- INTERFACE IVMDVDDrive Pc Virtual , propriedade ImageFile
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 275826aaea8dcb4f40427f2448a5edc86a992aefa4dc81648703a5f0a2948604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123738"
---
# <a name="ivmdvddriveimagefile-property"></a>Propriedade IVMDVDDrive::ImageFile

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o caminho completo do conjunto de arquivos de imagem para este dispositivo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a>Valor da propriedade

O caminho completo para o arquivo de imagem.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                            | Significado                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | A operação foi bem-sucedida.<br/>                                  |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                 | O parâmetro é **NULL.**<br/>                                     |
| <dl> <dt>E \_ FAIL</dt> <dt>0X80004005</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                              |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                        |
| <dl> <dt>VM \_ E \_ UNIDADE \_ INVÁLIDA</dt> <dt>0XA0040502</dt> </dl>      | O local do barramento para essa unidade não é válido.<br/>                  |
| <dl> <dt>VM \_ E \_ MEDIA WRONG TYPE \_ \_ 0XA00400728</dt> <dt></dt> </dl> | A mídia capturada por essa unidade de DVD não é um arquivo de imagem ISO.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Ocorreu um erro inesperado.<br/>                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive é definido como \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

