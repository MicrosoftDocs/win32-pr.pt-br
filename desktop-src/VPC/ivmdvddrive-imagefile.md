---
title: Propriedade ImageFile de IVMDVDDrive (VPCCOMInterfaces. h)
description: Recupera o caminho completo do conjunto de arquivos de imagem para este dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Propriedade ImageFile Virtual PC
- Propriedade ImageFile Virtual PC, interface IVMDVDDrive
- IVMDVDDrive da interface virtual PC, propriedade ImageFile
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
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824724"
---
# <a name="ivmdvddriveimagefile-property"></a>Propriedade IVMDVDDrive:: ImageFile

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                 | O parâmetro é **NULL**.<br/>                                     |
| <dl> <dt>E \_ FALHA</dt> <dt>0x80004005</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                              |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                        |
| <dl> <dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt> </dl>      | O local do barramento desta unidade não é válido.<br/>                  |
| <dl> <dt>VM \_ \_Mídia E \_ \_ tipo incorreto</dt> <dt>0xA00400728</dt> </dl> | A mídia capturada por esta unidade de DVD não é um arquivo de imagem ISO.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>         | Ocorreu um erro inesperado.<br/>                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

