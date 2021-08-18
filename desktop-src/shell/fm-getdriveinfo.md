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
ms.openlocfilehash: 39df15a4522e863fada40d3c964d709f40d2a26d01240aaefe51b09924b8c9ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459116"
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

## <a name="return-value"></a>Valor retornado

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

 

 




