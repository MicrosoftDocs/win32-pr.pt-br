---
description: Enviado por uma extensão do Gerenciador de Arquivos para recuperar informações da unidade da janela ativa do Gerenciador de Arquivos.
title: FM_GETDRIVEINFO mensagem (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842407"
---
# <a name="fm_getdriveinfo-message"></a>Mensagem \_ FM GETDRIVEINFO

Enviado por uma extensão do Gerenciador de Arquivos para recuperar informações da unidade da janela ativa do Gerenciador de Arquivos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

O endereço de uma estrutura [**\_ GETDRIVEINFO do FMS**](fms-getdriveinfo.md) que recebe informações de unidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um zero.

## <a name="remarks"></a>Comentários

Se 0xFFFFFFFF for retornado no **membro dwTotalSpace** ou **dwFreeSpace** da estrutura [**\_ GETDRIVEINFO do FMS,**](fms-getdriveinfo.md) a biblioteca de extensões deverá computar o valor ou os valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




