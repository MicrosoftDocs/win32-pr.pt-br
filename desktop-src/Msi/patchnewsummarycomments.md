---
description: A propriedade PATCHNEWSUMMARYCOMMENTS atualiza a propriedade Resumo dos comentários de uma instalação administrativa durante a aplicação de patch.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Propriedade PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751637"
---
# <a name="patchnewsummarycomments-property"></a>Propriedade PATCHNEWSUMMARYCOMMENTS

A propriedade **PATCHNEWSUMMARYCOMMENTS** atualiza a propriedade [**Resumo dos comentários**](comments-summary.md) de uma instalação administrativa durante a aplicação de patch. Essa propriedade só é definida por uma transformação em um arquivo. msp. O arquivo. msp deve incluir uma transformação que adiciona essa propriedade à [tabela de propriedades](property-table.md) e define seu valor. Em seguida, o instalador grava o valor de **PATCHNEWSUMMARYCOMMENTS** na propriedade [**Summary do número de revisão**](revision-number-summary.md) .

## <a name="remarks"></a>Comentários

As propriedades [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) são usadas para atualizar as informações de resumo quando um patch é instalado em uma imagem administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




