---
description: Definir o valor dessa política de sistema por computador como &\# 0034;1&0034;, permite que usuários não administrativas instalem aplicativos gerenciados de fontes armazenadas na mídia, como um \# CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8e280fbd4941c43221d2178811fe341d4f963657bc4e6e5c9e8a19ec31acf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821856"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

Definir o valor dessa [](system-policy.md) política de sistema por computador como "1", [](m-gly.md) permite que usuários não administrativas instalem aplicativos gerenciados de fontes armazenadas na mídia, como um CD-ROM. Consulte [Resiliência de origem.](source-resiliency.md) Por exemplo, se essa política for definida, um usuário nãoadministrativo poderá usar uma fonte de mídia para instalar aplicativos ou aplicativos atribuídos ou publicados que estão sendo instalados para todos os usuários. Definir essa política também permite que usuários não administrativos executem programas em privilégios localSystem durante uma instalação com privilégios elevados.

O valor padrão dessa política é 1 somente em computadores que executam Windows Vista e que não estão ingressados em um domínio. O padrão em outros computadores é que usuários não administrativas não podem instalar aplicativos gerenciados de uma fonte localizada na mídia.

Como essa política permite que os usuários que não são administradores instalem com privilégios que não têm por padrão, antes de definir essa política, você deve considerar se ela fornece um nível apropriado de segurança para o usuário. A configuração padrão é recomendada para garantir um ambiente seguro.

Para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and Digital Signatures and [Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation](downloading-an-installation-from-the-internet.md)from the Internet .

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios localSystem se eles têm um pacote do instalador do Windows que instala ou inicia esses programas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



