---
description: A propriedade de resumo contagem de páginas contém a versão mínima do instalador exigida pelo pacote de instalação.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Propriedade de Resumo de contagem de páginas
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749993"
---
# <a name="page-count-summary-property"></a>Propriedade de Resumo de contagem de páginas

A propriedade de **Resumo contagem de páginas** contém a versão mínima do instalador exigida pelo pacote de instalação. Para um mínimo de Windows Installer 2,0, essa propriedade deve ser definida como o inteiro 200. Para um mínimo de Windows Installer 3,0, essa propriedade deve ser definida como o inteiro 300. Para um mínimo de Windows Installer 3,1, essa propriedade deve ser definida como 301. Para um mínimo de Windows Installer 4,5, essa propriedade deve ser definida como 405. Para um mínimo de Windows Installer 5,0, essa propriedade deve ser definida como 500.

Para [pacotes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md), essa propriedade deve ser definida como o inteiro 200 ou superior. Para pacotes de Windows Installer de 64 bits na plataforma Arm64, essa propriedade deve ser definida como o inteiro 500 ou superior.

Para um pacote de transformação, a propriedade de **Resumo contagem de páginas** contém a versão mínima do instalador necessária para processar a transformação. Defina como o maior dos dois valores de propriedade de **Resumo de contagem de páginas** que pertencem aos bancos de dados usados para gerar a transformação.

Para um pacote de patch, a propriedade de **Resumo contagem de páginas** é definida como NULL.

Essa propriedade de resumo é necessária.

Essa propriedade pode ser usada para criar um pacote que pode ser instalado somente pela versão mínima ou posterior especificada do Windows Installer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




