---
description: Windows A versão 2,0 do instalador começa a procurar uma fonte, verificando o local de origem usado mais recentemente na lista de origem, a lista de fontes de rede, as fontes de mídia e, por fim, fontes de URL.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Política de resiliência de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4951c1183da8998986863fe5dae744fc58c23387306c91153b50ab63e38e0a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039706"
---
# <a name="source-resiliency-policy"></a>Política de resiliência de origem

O instalador começa a procurar uma fonte verificando o local de origem usado mais recentemente na lista de origem, a lista de fontes de rede, as fontes de mídia e, por fim, fontes de URL. Para obter mais informações, consulte [resiliência de origem](source-resiliency.md). Se a pesquisa falhar, o instalador poderá apresentar uma [caixa de diálogo de procura](browse-dialog.md) que permite ao usuário procurar a origem manualmente. A caixa de diálogo procurar não poderá ser exibida se os [níveis de interface do usuário](user-interface-levels.md) estiverem definidos como nenhum. Um administrador controla a exibição da caixa de diálogo Procurar para os usuários definindo a política do sistema.

com Windows Installer, os não administradores, por padrão, não podem usar a caixa de diálogo procurar para localizar fontes de aplicativos gerenciados na mídia e não podem instalar aplicativos gerenciados. Um administrador permite que um não administrador procure ou instale aplicativos gerenciados da mídia usando as políticas [AllowLockdownBrowse](allowlockdownbrowse.md) e [AllowLockdownMedia](allowlockdownmedia.md) . Um administrador desabilita a capacidade de procurar ou instalar aplicativos da mídia usando as políticas [DisAbleBrowse](disablebrowse.md) e [DisAbleMedia](disablemedia.md) .

a tabela a seguir resume o uso dessas políticas do sistema no Windows Installer.



| Política do sistema                                  | Aplicativo não gerenciado de usuário não-administrador                                                                                                             | Aplicativo gerenciado por usuário não administrador                                                                                                                 | Aplicativo gerenciado pelo administrador aplicativos não gerenciados                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Os usuários podem instalar aplicativos não gerenciados usando fontes localizadas na mídia. Os usuários podem procurar mídia para as fontes de aplicativos não gerenciados.<br/>    | Os usuários não podem instalar aplicativos gerenciados usando fontes localizadas na mídia. Os usuários podem procurar mídia para as fontes de aplicativos gerenciados.<br/>      | Os administradores podem instalar aplicativos usando fontes localizadas na mídia. Os administradores podem procurar mídia para as fontes de aplicativos.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Os usuários podem instalar aplicativos não gerenciados usando fontes localizadas na mídia. Os usuários podem procurar mídia para as fontes de aplicativos não gerenciados.<br/>    | Os usuários podem instalar aplicativos gerenciados usando fontes localizadas na mídia. Os usuários não podem procurar mídia para as fontes de aplicativos gerenciados.<br/>      | Os administradores podem instalar aplicativos usando fontes localizadas na mídia. Os administradores podem procurar mídia para as fontes de aplicativos.<br/>    |
| *Padrão*                                      | Os usuários podem instalar aplicativos não gerenciados usando fontes localizadas na mídia. Os usuários podem procurar mídia para as fontes de aplicativos não gerenciados.<br/>    | Os usuários não podem instalar aplicativos gerenciados usando fontes localizadas na mídia. Os usuários não podem procurar mídia para as fontes de aplicativos gerenciados.<br/>   | Os administradores podem instalar aplicativos usando fontes localizadas na mídia. Os administradores podem procurar mídia para as fontes de aplicativos.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Os usuários podem instalar aplicativos não gerenciados usando fontes localizadas na mídia. Os usuários não podem navegar pela mídia para as fontes de aplicativos não gerenciados.<br/> | Os usuários não podem instalar aplicativos gerenciados usando fontes localizadas na mídia. Os usuários não podem procurar mídia para as fontes de aplicativos gerenciados. .<br/> | Os administradores podem instalar aplicativos usando fontes localizadas na mídia. Os administradores não podem navegar pela mídia para as fontes de aplicativos.<br/> |
| [DisAbleMedia](disablemedia.md)               | Os usuários não podem instalar aplicativos não gerenciados usando fontes localizadas na mídia. Os usuários podem procurar mídia para as fontes de aplicativos não gerenciados.<br/> | Os usuários não podem instalar aplicativos gerenciados usando fontes localizadas na mídia. Os usuários não podem procurar mídia para as fontes de aplicativos gerenciados.<br/>   | Os administradores não podem instalar aplicativos usando fontes localizadas na mídia. Os administradores podem procurar mídia para as fontes de aplicativos.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




