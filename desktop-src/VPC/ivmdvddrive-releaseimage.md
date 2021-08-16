---
title: Método IvMDVDDrive ReleaseImage (VPCCOMInterfaces.h)
description: Libera uma imagem ISO capturada da unidade de DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- Pc Virtual do método ReleaseImage
- Computador Virtual do método ReleaseImage, interface IVMDVDDrive
- INTERFACE IVMDVDDrive pc virtual , método ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0fc61212ff07f3a0279dfdb38517d4ab2d265d89e15aaad61450e3effd9ec9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345728"
---
# <a name="ivmdvddrivereleaseimage-method"></a>Método IVMDVDDrive::ReleaseImage

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera uma imagem ISO capturada da unidade de DVD.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                         | Descrição                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | A operação foi bem-sucedida.<br/>                                      |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                            |
| <dl> <dt>**VM \_ E \_ MEDIA WRONG TYPE \_ \_ 0XA00400728**</dt> <dt></dt> </dl> | A mídia capturada no momento não é uma unidade de disco de host.<br/>             |
| <dl> <dt>**VM \_ E \_ UNIDADE \_ INVÁLIDA**</dt> <dt>0XA0040502</dt> </dl>      | A unidade não pôde ser inicializada devido a um local de barramento inválido.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>         | Ocorreu um erro inesperado.<br/>                                  |



 

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

 

