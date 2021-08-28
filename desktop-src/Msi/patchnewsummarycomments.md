---
description: A propriedade PATCHNEWSUMMARYCOMMENTS atualiza a propriedade Resumo de Comentários de uma instalação administrativa durante a adoção de patch.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Propriedade PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef7a67b960b41e55caf5251a33ac6d3198147b92bcab895a2ca711af330acd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074776"
---
# <a name="patchnewsummarycomments-property"></a>Propriedade PATCHNEWSUMMARYCOMMENTS

A **propriedade PATCHNEWSUMMARYCOMMENTS** atualiza a propriedade [**Resumo**](comments-summary.md) de Comentários de uma instalação administrativa durante a adoção de patch. Essa propriedade só é definida por uma transformação em um arquivo .msp. O arquivo .msp deve incluir uma transformação que adiciona essa propriedade à tabela [Property](property-table.md) e define seu valor. Em seguida, o instalador grava o valor **de PATCHNEWSUMMARYCOMMENTS** na propriedade [**Resumo do Número de**](revision-number-summary.md) Revisão.

## <a name="remarks"></a>Comentários

As [**propriedades PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) são usadas para atualizar as informações resumidas quando um patch é instalado em uma imagem administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




