---
description: Definir a política TransformsSecure como 1 informa ao instalador que as transformaçãos devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tenha acesso de gravação.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: TransformsSecure Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6300a25db8e80003ff2a03afd56b168b9697f92764f16a26e99860c0a27796bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500287"
---
# <a name="transformssecure-policy"></a>TransformsSecure Policy

Definir a política TransformsSecure como 1 informa ao instalador que as transformaçãos devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tenha acesso de gravação. Definir essa política é o mesmo que definir a [propriedade TRANSFORMSSECURE,](transformssecure.md) exceto que o escopo é diferente. A configuração de TransformaçãoSeçõesA política doSecure se aplica a todos os pacotes instalados em um determinado computador. Definir a propriedade TRANSFORMSSECURE se aplica ao pacote, independentemente do computador.

A finalidade dessa política é fornecer armazenamento de transformação segura com usuários de viagem do Windows 2000. A partir do Windows Server 2003, o valor padrão dessa política é 1.

Quando essa política é definida, uma instalação [de manutenção](maintenance-installation.md) só pode usar a transformação do cache protegido. Caso o instalador descubra que a transformação está ausente no computador local, o instalador tenta restaurar a transformação. Para que o instalador restaure a transformação, a transformação segura deve residir em uma fonte autorizada na lista de origem do pacote de instalação. Para obter mais informações, consulte [Resiliência de origem.](source-resiliency.md) A instalação de manutenção falhará se a transformação não estiver disponível ou não puder ser carregada.

No Windows Server 2003, se essa política não estiver definida, o comportamento padrão será armazenar as transformares em um local seguro. Em todas as versões anteriores ao Windows Server 2003, se a política não estiver definida, o comportamento padrão será armazenar as transformação no perfil de usuários.

Confira também [As Transformaçãos Protegidas](secured-transforms.md) para obter mais informações.

Windows O instalador interpreta que [a política TransformsAtSource](transformsatsource-policy.md) é a mesma que a política TransformsSecure.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



