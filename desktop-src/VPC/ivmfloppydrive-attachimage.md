---
title: Método IVMFloppyDrive AttachImage (VPCCOMInterfaces.h)
description: Anexa uma imagem de mídia disquete no host à unidade de disquete da máquina virtual.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Computador Virtual do método AttachImage
- Método AttachImage Pc Virtual, interface IVMFloppyDrive
- INTERFACE IVMFloppyDrive pc virtual , método AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21af305d0e7441fc931765795bb4e5d0785a211af6806ee80fd679d6f487b218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595710"
---
# <a name="ivmfloppydriveattachimage-method"></a>Método IVMFloppyDrive::AttachImage

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa uma imagem de mídia disquete no host à unidade de disquete da máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mediaImagePath* \[ Em\]
</dt> <dd>

O caminho completo para a imagem de mídia de disquete a ser anexada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O *parâmetro mediaImagePath* não é válido.<br/>                                                                                 |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                    | O parâmetro é **NULL.**<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | Não há memória suficiente disponível para concluir essa solicitação.<br/>                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0X8007006F</dt> </dl> | O caminho especificado pelo parâmetro *mediaImagePath* é muito longo. O caminho deve ter menos de **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0X8007007B</dt> </dl>    | O *parâmetro mediaImagePath* contém um caractere inválido (um de " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ BAD PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | O *parâmetro mediaImagePath* especifica um caminho vazio ou relativo. Um caminho absoluto é necessário.<br/>                            |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | A configuração dessa máquina virtual não é válida ou não pode ser encontrada.<br/>                                                  |
| <dl> <dt>**VM \_ A \_ CAPTURA DE IMAGEM E \_ \_ FALHA**</dt> <dt>0XA00400650</dt> </dl>                  | Não foi possível capturar o arquivo de imagem especificado.<br/>                                                                              |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFloppyDrive é definido como \_ 661abee6-112a-4ed9-ertf-3c874969f10e<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

