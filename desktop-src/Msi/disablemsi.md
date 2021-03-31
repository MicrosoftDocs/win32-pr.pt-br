---
description: Se o valor dessa política do sistema por máquina estiver definido como &\# 0034; 2&\# 0034; o instalador estará sempre desabilitado para todos os aplicativos. Se esse valor de política for definido como &\# 0034; 1&\# 0034;, o instalador será desabilitado para aplicativos não gerenciados, mas ainda estará habilitado para aplicativos gerenciados.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011155"
---
# <a name="disablemsi"></a>DisableMSI

Se o valor dessa [política do sistema](system-policy.md) por máquina estiver definido como "2", o instalador estará sempre desabilitado para todos os aplicativos. Se esse valor de política for definido como "1", o instalador será desabilitado para aplicativos não gerenciados, mas ainda estará habilitado para aplicativos gerenciados.

A tabela a seguir lista as possíveis configurações.



| DisableMSI | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Default*  | No Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 e Windows Server 2008 R2, se o valor da política for nulo, ausente ou qualquer número diferente de 1 ou 2, o Windows Installer será habilitado para aplicativos gerenciados. As instalações de aplicativos não gerenciados são bloqueadas.<br/> No Windows XP, no Windows Vista e no Windows 7, a Windows Installer está habilitada para todos os aplicativos. Todas as operações de instalação são permitidas.<br/> |
| 0          | O Windows Installer está habilitado para todos os aplicativos. Todas as operações de instalação são permitidas.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | O Windows Installer está desabilitado para aplicativos não gerenciados, mas ainda está habilitado para aplicativos gerenciados. As instalações não elevadas por usuário são bloqueadas. Instalações elevadas por usuário e por máquina são permitidas.                                                                                                                                                                                                                        |
| 2          | O Windows Installer está sempre desabilitado para todos os aplicativos. Nenhuma instalação é permitida, incluindo reparos, reinstalação ou instalações sob demanda.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




