---
description: Definir o valor dessa política do sistema por máquina para &\# 0034; 1&\# 0034;, permite que usuários não administrativos instalem aplicativos gerenciados de fontes armazenadas em mídia, como um CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837682"
---
# <a name="allowlockdownmedia"></a>AllowLockdownMedia

Definir o valor dessa [política de sistema](system-policy.md) por máquina como "1" permite que usuários não administrativos instalem [*aplicativos gerenciados*](m-gly.md) de fontes armazenadas em mídia, como um CD-ROM. Consulte [resiliência da origem](source-resiliency.md). Por exemplo, se essa política estiver definida, um usuário não administrativo poderá usar uma fonte de mídia para instalar aplicativos atribuídos ou publicados ou aplicativos que estão sendo instalados para todos os usuários. Definir essa política também permite que usuários não administrativos executem programas em privilégios LocalSystem durante uma instalação elevada.

O valor padrão dessa política é 1 somente em computadores que executam o Windows Vista e que não fazem parte de um domínio. O padrão em outros computadores é que usuários não-administrativos não podem instalar aplicativos gerenciados de uma origem localizada na mídia.

Como essa política permite que os usuários que não são administradores instalem com privilégios que eles não têm, por padrão, antes de definir essa política, você deve considerar se ele fornece um nível apropriado de segurança para o usuário. A configuração padrão é recomendada para garantir um ambiente seguro.

Para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [diretrizes para criar instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md) e [baixar uma instalação da Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Definir essa política também permite que usuários não administrativos executem programas arbitrários em privilégios LocalSystem se tiverem um pacote Windows Installer que instala ou inicia esses programas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> <dt>

[AllowLockdownBrowse](allowlockdownbrowse.md)
</dt> </dl>

 

 



