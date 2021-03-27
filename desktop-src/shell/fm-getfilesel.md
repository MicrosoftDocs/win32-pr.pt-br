---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa).
title: Mensagem de FM_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828303"
---
# <a name="fm_getfilesel-message"></a>\_Mensagem GETFILESEL de FM

Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*index* 
</dt> <dd>

O índice de base zero do arquivo selecionado a ser recuperado.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

O endereço de uma [**estrutura \_ GETFILESEL do FMS**](fms-getfilesel.md) que recebe informações sobre a seleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice de base zero do arquivo selecionado que foi recuperado.

## <a name="remarks"></a>Comentários

Uma extensão pode usar a [**mensagem \_ GETSELCOUNT de FM**](fm-getselcount.md) para recuperar a contagem de arquivos selecionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNTLFN FM**](fm-getselcountlfn.md)
</dt> </dl>

 

 




