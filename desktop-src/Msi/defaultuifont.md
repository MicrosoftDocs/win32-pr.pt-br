---
description: A propriedade DefaultUIFont define o estilo de fonte padrão usado para controles. Para especificar o padrão, defina DefaultUIFont como um dos estilos predefinidos na tabela TextStyle na tabela de propriedades.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propriedade DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750008"
---
# <a name="defaultuifont-property"></a>Propriedade DefaultUIFont

A propriedade **DefaultUIFont** define o estilo de fonte padrão usado para controles. Para especificar o padrão, defina **DefaultUIFont** como um dos estilos predefinidos na [tabela TextStyle](textstyle-table.md) na [tabela de propriedades](property-table.md).

## <a name="remarks"></a>Comentários

A propriedade **DefaultUIFont** de cada pacote de instalação com uma interface do usuário deve ser definida na [tabela de propriedades](property-table.md) para um dos estilos predefinidos listados na [tabela TextStyle](textstyle-table.md). Se essa propriedade não for especificada, o instalador usará a fonte do sistema. Isso pode fazer com que o instalador exiba incorretamente cadeias de caracteres de texto quando a página de código do pacote for diferente da página de código padrão da interface do usuário.

O texto e o estilo de fonte de um controle podem ser definidos conforme descrito em [adicionando controles e texto](adding-controls-and-text.md). Se a cadeia de caracteres listada na coluna texto da [tabela de controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md) não especificar o estilo da fonte, o controle usará o valor da propriedade **DefaultUIFont** como o estilo da fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




