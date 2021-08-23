---
description: A propriedade MsiHiddenProperties pode ser usada para impedir que o instalador exibe senhas ou outras informações confidenciais no arquivo de log.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propriedade MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acea21b946a4169748c96970143d6c44c6bf682ce6f6a8e4624791c52d0ba813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628095"
---
# <a name="msihiddenproperties-property"></a>Propriedade MsiHiddenProperties

A **propriedade MsiHiddenProperties** pode ser usada para impedir que o instalador exibe senhas ou outras informações confidenciais no arquivo de log. Para impedir que uma propriedade seja escrita no arquivo de log, de definido o valor da propriedade **MsiHiddenProperties** como o nome da propriedade que você deseja ocultar. Você pode ocultar várias propriedades especificando uma cadeia de caracteres de nomes de propriedade delimitados por ponto e vírgula (;).

> [!Note]  
> Quando a [política de depuração](debug.md) for definida como um valor de 7, o instalador gravará informações inseridas em uma linha de comando no log. Isso torna as propriedades públicas inseridas em uma linha de comando visíveis mesmo que a propriedade seja incluída na **propriedade MsiHiddenProperties.** Isso pode tornar as informações confidenciais inseridas em uma linha de comando visíveis no log. Para obter mais informações, [consulte Impedindo que informações confidenciais são escritas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




