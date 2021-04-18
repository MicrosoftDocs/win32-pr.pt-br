---
description: A propriedade PATCHNEWPACKAGECODE atualiza a propriedade Resumo do número de revisão de uma imagem administrativa durante a aplicação de patch.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propriedade PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756897"
---
# <a name="patchnewpackagecode-property"></a>Propriedade PATCHNEWPACKAGECODE

A propriedade **PATCHNEWPACKAGECODE** atualiza a propriedade [**Resumo do número de revisão**](revision-number-summary.md) de uma imagem administrativa durante a aplicação de patch. Essa propriedade só é definida por uma transformação em um arquivo. msp. O arquivo. msp deve incluir uma transformação que adiciona essa propriedade à [tabela de propriedades](property-table.md) e define seu valor. Em seguida, o instalador grava o valor de **PATCHNEWPACKAGECODE** na propriedade **Summary do número de revisão** .

## <a name="remarks"></a>Comentários

As propriedades **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) são usadas para atualizar as informações de resumo quando um patch é instalado em uma imagem administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




