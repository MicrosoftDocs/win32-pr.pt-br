---
description: A propriedade MsiHiddenProperties pode ser usada para impedir que o instalador exiba senhas ou outras informações confidenciais no arquivo de log.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propriedade MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766868"
---
# <a name="msihiddenproperties-property"></a>Propriedade MsiHiddenProperties

A propriedade **MsiHiddenProperties** pode ser usada para impedir que o instalador exiba senhas ou outras informações confidenciais no arquivo de log. Para impedir que uma propriedade seja gravada no arquivo de log, defina o valor da propriedade **MsiHiddenProperties** como o nome da propriedade que você deseja ocultar. Você pode ocultar várias propriedades especificando uma cadeia de caracteres de nomes de propriedade delimitada por ponto-e-vírgula (;).

> [!Note]  
> Quando a política de [depuração](debug.md) for definida com um valor de 7, o instalador gravará as informações inseridas em uma linha de comando no log. Isso torna as propriedades públicas inseridas em uma linha de comando visíveis, mesmo que a propriedade seja incluída na propriedade **MsiHiddenProperties** . Isso pode tornar as informações confidenciais inseridas em uma linha de comando visíveis no log. Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




