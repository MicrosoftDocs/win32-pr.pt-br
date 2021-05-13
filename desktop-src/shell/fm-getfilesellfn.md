---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa). O arquivo selecionado pode ter um nome de arquivo longo.
title: Mensagem de FM_GETFILESELLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842387"
---
# <a name="fm_getfilesellfn-message"></a>\_Mensagem GETFILESELLFN de FM

Enviado por uma extensão do Gerenciador de arquivos para recuperar informações sobre um arquivo selecionado na janela do Active File Manager (a janela do diretório ou a janela de resultados da pesquisa). O arquivo selecionado pode ter um nome de arquivo longo.

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

Somente extensões que dão suporte a nomes de arquivo longos (por exemplo, extensões com reconhecimento de rede) devem usar essa mensagem.

Uma extensão pode usar a [**mensagem \_ GETSELCOUNTLFN de FM**](fm-getselcountlfn.md) para recuperar a contagem de arquivos selecionados.

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

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




