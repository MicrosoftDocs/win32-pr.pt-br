---
title: Método IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Anexa uma imagem de mídia de disquete no host à unidade de disquete da máquina virtual.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- AttachImage do método virtual PC
- Método AttachImage Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, método AttachImage
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
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918300"
---
# <a name="ivmfloppydriveattachimage-method"></a>Método IVMFloppyDrive:: AttachImage

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa uma imagem de mídia de disquete no host à unidade de disquete da máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mediaImagePath* \[ no\]
</dt> <dd>

O caminho completo para a imagem de mídia de disquete a ser anexada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O parâmetro *mediaImagePath* não é válido.<br/>                                                                                 |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro é **NULL**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl>      | Não há memória suficiente disponível para concluir esta solicitação.<br/>                                                               |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelo parâmetro *mediaImagePath* é muito longo. O caminho deve ser menor que **o \_ caminho máximo** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *mediaImagePath* contém um caractere inválido (um de " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *mediaImagePath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                            |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                            | A configuração desta máquina virtual não é válida ou não foi encontrada.<br/>                                                  |
| <dl> <dt>**VM \_ 0xA00400650 \_ de \_ \_ falha de captura de imagem E**</dt> <dt></dt> </dl>                  | Não foi possível capturar o arquivo de imagem especificado.<br/>                                                                              |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

