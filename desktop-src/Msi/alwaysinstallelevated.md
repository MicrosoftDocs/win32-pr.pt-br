---
description: Instale um Windows instalador com privilégios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc015dad8096db16d8b70238a5fd7e07544b83f9a9e3d1a5045be9d12bbb30cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650236"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

Você pode usar a política AlwaysInstallElevated para instalar um Windows instalador com privilégios elevados (sistema).

**Aviso: **

Essa opção é equivalente a conceder direitos administrativos completos, o que pode representar um grande risco à segurança. A Microsoft não quer usar essa configuração.

Para instalar um pacote com privilégios elevados (sistema), de definido o valor AlwaysInstallElevated como "1" em ambas as chaves do Registro a seguir:

**HKEY \_ Instalador \_ do** \\  \\  \\ **Microsoft** \\ **Windows** Políticas de Software \\ **DO USUÁRIO ATUAL**

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **Windows** \\ **LOCAL** MACHINE

Se o valor AlwaysInstallElevated não estiver definido como "1" em ambas as chaves do Registro anteriores, o instalador usará privilégios elevados para instalar aplicativos gerenciados e usará o nível de privilégio do usuário atual para aplicativos não gerenciados.

Como essa política permite que os usuários instalem aplicativos que exigem acesso a diretórios e chaves do Registro para os quais o usuário pode não ter permissão para exibir ou alterar, você deve considerar se ele fornece aos usuários um nível apropriado de segurança. Definir essa política direciona Windows Instalador para usar permissões do sistema quando ele instala o aplicativo no sistema. Se essa política não for definida, os aplicativos não distribuídos pelo administrador serão instalados usando os privilégios do usuário e somente os aplicativos gerenciados obterão privilégios elevados.

Observe que, depois que a política por computador para AlwaysInstallElevated for habilitada, qualquer usuário poderá definir sua configuração por usuário.

## <a name="remarks"></a>Comentários

Para obter informações sobre a interação dessa política com fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



