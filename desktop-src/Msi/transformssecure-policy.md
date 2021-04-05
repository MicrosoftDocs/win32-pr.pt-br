---
description: Definir a política TransformsSecure como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Política de TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826781"
---
# <a name="transformssecure-policy"></a>Política de TransformsSecure

Definir a política TransformsSecure como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação. Definir essa política é o mesmo que definir a [Propriedade TRANSFORMSSECURE](transformssecure.md) , exceto que o escopo é diferente. A configuração da política TransformsSecure se aplica a todos os pacotes instalados em um determinado computador. A definição da propriedade TRANSFORMSSECURE se aplica ao pacote, independentemente do computador.

A finalidade dessa política é fornecer armazenamento de transformação seguro com usuários viajando do Windows 2000. A partir do Windows Server 2003, o valor padrão dessa política é 1.

Quando essa política é definida, uma [instalação de manutenção](maintenance-installation.md) só pode usar a transformação do cache protegido. Caso o instalador ache que a transformação está ausente no computador local, o instalador tentará restaurar a transformação. Para que o instalador restaure a transformação, a transformação segura deve residir em uma fonte autorizada na lista de origem do pacote de instalação. Para obter mais informações, consulte [resiliência de origem](source-resiliency.md). A instalação de manutenção falhará se a transformação não estiver disponível ou não puder ser carregada.

No Windows Server 2003, se essa política não estiver definida, o comportamento padrão será armazenar as transformações em um local seguro. Em todas as versões anteriores ao Windows Server 2003, se a política não estiver definida, o comportamento padrão será armazenar as transformações no perfil de usuários.

Consulte também [transformações protegidas](secured-transforms.md) para obter mais informações.

Windows Installer interpreta a [política TransformsAtSource](transformsatsource-policy.md) para ser a mesma que a política TransformsSecure.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



