---
description: A propriedade PATCHNEWPACKAGECODE atualiza a propriedade Resumo do Número de Revisão de uma imagem administrativa durante a adoção de patch.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propriedade PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d7e64729643fa1b6449838496416d10e1ec12374762b3f702b306a146338f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926156"
---
# <a name="patchnewpackagecode-property"></a>Propriedade PATCHNEWPACKAGECODE

A **propriedade PATCHNEWPACKAGECODE** atualiza a propriedade [**Resumo do**](revision-number-summary.md) Número de Revisão de uma imagem administrativa durante a adoção de patch. Essa propriedade só é definida por uma transformação em um arquivo .msp. O arquivo .msp deve incluir uma transformação que adiciona essa propriedade à tabela [Property](property-table.md) e define seu valor. Em seguida, o instalador grava o valor **de PATCHNEWPACKAGECODE** na propriedade **Resumo do Número de** Revisão.

## <a name="remarks"></a>Comentários

As **propriedades PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) são usadas para atualizar as informações resumidas quando um patch é instalado em uma imagem administrativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




