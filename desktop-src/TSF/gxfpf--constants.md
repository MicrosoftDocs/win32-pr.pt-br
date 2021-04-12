---
title: Constantes de GXFPF_ (Textstor. h)
description: GXFPF \_ \ constantes especifique a posição do caractere a ser retornada com base nas coordenadas da tela do ponto em relação a uma caixa delimitadora de caracteres.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454845"
---
# <a name="gxfpf_-constants"></a>\_ \* Constantes GXFPF

\_ \* As constantes GXFPF especificam a posição do caractere a ser retornada com base nas coordenadas da tela do ponto em relação a uma caixa delimitadora de caracteres.



| Constante/valor                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <dt>**GXFPF \_ ROUND \_ mais próximo**</dt> <dt>(0x1)</dt> </dl> | Se as coordenadas da tela do ponto estiverem contidas em uma caixa delimitadora de caracteres, a posição do caractere retornada será a borda delimitadora mais próxima das coordenadas da tela do ponto.<br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <dt>**GXFPF \_ A mais próxima**</dt> <dt>(0x2)</dt> </dl>                    | Se as coordenadas da tela do ponto não estiverem contidas em uma caixa delimitadora de caracteres, a posição do caractere mais próxima será retornada.<br/>                                                      |



## <a name="remarks"></a>Comentários

Os parâmetros *dwFlags* dos métodos [ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) e [ITfContextOwner:: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usam essas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





