---
title: Identificadores de tipo de espaço de cores
description: Essas constantes especificam o tipo de uma matriz de espaço de cores de PostScript 2. Os valores a seguir são tipos de matriz de espaço de cores válidos.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105795511"
---
# <a name="color-space-type-identifiers"></a>Identificadores de tipo de espaço de cores

Essas constantes especificam o tipo de uma matriz de espaço de cores de PostScript 2. Os valores a seguir são tipos de matriz de espaço de cores válidos.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedA do perfil monocromático.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_cinza CSA**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedA do perfil monocromático.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**ABC de CSA \_**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedABC do perfil RGB ou L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**definição de CSA \_**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedDEF do perfil RGB ou L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**do CSA \_ RGB**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedDEF seguida por uma matriz de espaço de cores CIEBasedABC do perfil RGB. Na execução, se a impressora não der suporte a espaços de cores CIEBasedDEF, a função usará a definição CIEBasedABC.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**\_Laboratório CSA**
</dt> <dd> <dl> <dt>



Obtém uma matriz de espaço de cores CIEBasedABC do <sup>\*</sup> perfil L a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**\_DEFG CSA**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedDEFG do perfil CMYK.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**
</dt> <dd> <dl> <dt>



Obtenha uma matriz de espaço de cores CIEBasedCMYK do perfil CMYK.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Constantes de ICM](wcs-constants.md)
</dt> </dl>

 

 




