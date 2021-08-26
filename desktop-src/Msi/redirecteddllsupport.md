---
description: O instalador define a propriedade RedirectedDLLSupport se a plataforma do sistema que executa a instalação dá suporte a Componentes Isolados.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propriedade RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24da5990645d4c27120c3a010cc517475ba6e706c2fb41d69a024d15ca524549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979316"
---
# <a name="redirecteddllsupport-property"></a>Propriedade RedirectedDLLSupport

O instalador define a propriedade **RedirectedDLLSupport** se a plataforma do sistema que executa a instalação dá suporte a [Componentes Isolados](isolated-components.md).

O instalador define a propriedade **RedirectedDLLSupport** como um valor de 1 se o sistema que executa a instalação dá suporte a Componentes Isolados [com](isolated-components.md) base em . Arquivos LOCAIS. O instalador define a propriedade **RedirectedDLLSupport** como um valor de 2 se o sistema que executa a instalação dá suporte ao isolamento usando qualquer um dos . Arquivos LOCAIS ou assemblies lado a lado do Win32.

A **propriedade RedirectedDLLSupport** pode ser usada para condicionar a ação [IsolateComponents](isolatecomponents-action.md) na tabela [InstallUISequence](installuisequence-table.md) ou [na tabela InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




