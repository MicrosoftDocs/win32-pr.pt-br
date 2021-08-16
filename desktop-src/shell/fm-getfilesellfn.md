---
description: Enviado por uma extensão do Gerenciador de Arquivos para recuperar informações sobre um arquivo selecionado da janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa). O arquivo selecionado pode ter um nome de arquivo longo.
title: FM_GETFILESELLFN mensagem (Wfext.h)
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
ms.openlocfilehash: 2074fb1e631edf1795b8f0d15ea9f0d40e90556d527899873ef88195c2367576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860763"
---
# <a name="fm_getfilesellfn-message"></a>Mensagem \_ FM GETFILESELLFN

Enviado por uma extensão do Gerenciador de Arquivos para recuperar informações sobre um arquivo selecionado da janela ativa do Gerenciador de Arquivos (a janela diretório ou a janela Resultados da Pesquisa). O arquivo selecionado pode ter um nome de arquivo longo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*index* 
</dt> <dd>

O índice baseado em zero do arquivo selecionado a ser recuperado.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

O endereço de uma [**estrutura \_ GETFILESEL**](fms-getfilesel.md) DO FMS que recebe informações sobre a seleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice baseado em zero do arquivo selecionado que foi recuperado.

## <a name="remarks"></a>Comentários

Somente extensões que suportam nomes de arquivo longos (por exemplo, extensões com suporte à rede) devem usar essa mensagem.

Uma extensão pode usar [**a mensagem FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) para recuperar a contagem de arquivos selecionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FM \_ GETFILESEL**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ GETSELCOUNT**](fm-getselcount.md)
</dt> </dl>

 

 




