---
description: A propriedade PATCHNEWSUMMARYSUBJECT atualiza a propriedade Resumo da Assunto de uma imagem administrativa durante a a patch.
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: Propriedade PATCHNEWSUMMARYSUBJECT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912fe9ea21605625135b385a400fd5136c993c1d0dd0e3bfadd6a2b6699d21e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926157"
---
# <a name="patchnewsummarysubject-property"></a>Propriedade PATCHNEWSUMMARYSUBJECT

A **propriedade PATCHNEWSUMMARYSUBJECT** atualiza a propriedade [**Resumo**](subject-summary.md) da Assunto de uma imagem administrativa durante a a patch. Essa propriedade só é definida por uma transformação em um arquivo .msp. O arquivo .msp deve incluir uma transformação que adiciona essa propriedade à tabela [Property](property-table.md) e define seu valor. Em seguida, o instalador grava o valor **de PATCHNEWSUMMARYSUBJECT** na propriedade [**Resumo do Número de**](revision-number-summary.md) Revisão.

## <a name="remarks"></a>Comentários

As [**propriedades PATCHNEWPACKAGECODE**](patchnewpackagecode.md), [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e **PATCHNEWSUMMARYSUBJECT** são usadas para atualizar as informações resumidas quando um patch é instalado em uma imagem administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




