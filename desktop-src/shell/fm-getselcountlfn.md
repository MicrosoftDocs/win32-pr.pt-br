---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar o número de arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela do diretório ou a janela de resultados da pesquisa). A contagem inclui arquivos que têm nomes de arquivo longos.
title: Mensagem de FM_GETSELCOUNTLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 0a09ca8315405f06db091b27b9d326090796504c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104989002"
---
# <a name="fm_getselcountlfn-message"></a>\_Mensagem GETSELCOUNTLFN de FM

Enviado por uma extensão do Gerenciador de arquivos para recuperar o número de arquivos selecionados na janela do Gerenciador de arquivos ativa (a janela do diretório ou a janela de resultados da pesquisa). A contagem inclui arquivos que têm nomes de arquivo longos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de arquivos selecionados.

## <a name="remarks"></a>Comentários

Somente extensões que dão suporte a nomes de arquivo longos (por exemplo, extensões com reconhecimento de rede) devem usar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




