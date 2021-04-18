---
description: O instalador definirá a propriedade RedirectedDLLSupport se a plataforma do sistema que executa a instalação do oferecer suporte a componentes isolados.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propriedade RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780946"
---
# <a name="redirecteddllsupport-property"></a>Propriedade RedirectedDLLSupport

O instalador definirá a propriedade **RedirectedDLLSupport** se a plataforma do sistema que executa a instalação do oferecer suporte a [componentes isolados](isolated-components.md).

O instalador definirá a propriedade **RedirectedDLLSupport** com um valor de 1 se o sistema que estiver executando a instalação oferecer suporte a [componentes isolados](isolated-components.md) baseados em. Arquivos locais. O instalador definirá a propriedade **RedirectedDLLSupport** com um valor de 2 se o sistema que executa a instalação do oferecer suporte ao isolamento usando qualquer um dos dois. Arquivos locais ou assemblies lado a lado do Win32.

A propriedade **RedirectedDLLSupport** pode ser usada para condição da [ação IsolateComponents](isolatecomponents-action.md) na [tabela InstallUISequence](installuisequence-table.md) ou na [tabela InstallExecuteSequence](installexecutesequence-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




