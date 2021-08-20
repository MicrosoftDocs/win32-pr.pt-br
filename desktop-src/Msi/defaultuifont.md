---
description: A propriedade DefaultUIFont define o estilo de fonte padrão usado para controles. Para especificar o padrão, de definido DefaultUIFont como um dos estilos predefinidos na tabela TextStyle na tabela Property.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propriedade DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46bf4c432a0e75c933136cc11e1dd8a55cc6a4cdf2f09c923804132b743e88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289576"
---
# <a name="defaultuifont-property"></a>Propriedade DefaultUIFont

A **propriedade DefaultUIFont** define o estilo de fonte padrão usado para controles. Para especificar o padrão, de definir **DefaultUIFont como** um dos estilos predefinidos na [tabela TextStyle](textstyle-table.md) na [tabela Property](property-table.md).

## <a name="remarks"></a>Comentários

A **propriedade DefaultUIFont** de cada pacote de instalação [](property-table.md) com uma interface do usuário deve ser definida na tabela Propriedade para um dos estilos predefinidos listados na [tabela TextStyle](textstyle-table.md). Se essa propriedade não for especificada, o instalador usará a fonte System. Isso pode fazer com que o instalador exibe incorretamente cadeias de caracteres de texto quando a página de código do pacote é diferente da página de código de interface do usuário padrão do usuário.

O estilo de texto e fonte de um controle pode ser definido conforme descrito em [Adicionando controles e texto.](adding-controls-and-text.md) Se a cadeia de caracteres listada na coluna Texto da tabela [Control](control-table.md) ou [BBControl](bbcontrol-table.md) não especificar o estilo da fonte, o controle usará o valor da propriedade **DefaultUIFont** como o estilo da fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




