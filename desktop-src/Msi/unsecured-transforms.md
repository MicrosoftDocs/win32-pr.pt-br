---
description: As transformações que não foram protegidas, conforme descrito em transformações seguras, são transformações não seguras por padrão.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformações não seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bb234a0cdee852d3a5e1717642f5325283a571b740c9d7b4a5f6901afb52c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499606"
---
# <a name="unsecured-transforms"></a>Transformações não seguras

As transformações que não foram protegidas, conforme descrito em [transformações seguras](secured-transforms.md) , são transformações não seguras por padrão.

Para aplicar uma transformação não segura ao instalar um pacote, passe os nomes de arquivo de transformação na propriedade [**TRANSformações**](transforms.md) ou na cadeia de caracteres de linha de comando. Não inicie a cadeia de caracteres com os caracteres @ ou \| ou defina a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) . Observe que você não pode combinar transformações não seguras e [transformações protegidas](secured-transforms.md) na mesma lista de transformações.

Se o pacote estiver instalado ou anunciado no [contexto de instalação](installation-context.md)por usuário e tiver transformações desprotegidas, o instalador salvará a origem da transformação na pasta dados do aplicativo no perfil do usuário. Isso permite que um usuário mantenha a personalização de um produto durante a movimentação entre computadores.

Se o pacote estiver instalado ou anunciado no [contexto de instalação](installation-context.md)por máquina e usar transformações não seguras, o instalador salvará a origem da transformação na pasta% windir% \\ Installer.

Durante uma primeira instalação do pacote, o instalador primeiro procura a transformação na origem fornecida pela propriedade [**TRANSformações**](transforms.md) ou cadeia de caracteres de linha de comando. Se essa fonte não estiver disponível, o instalador pesquisará a transformação na origem do pacote ao lado do arquivo de .msi.

Durante uma [instalação de manutenção](maintenance-installation.md), o instalador pesquisa a transformação no local do cache. Se a cópia armazenada em cache da transformação ficar indisponível, o instalador pesquisará a transformação na origem do pacote ao lado do arquivo de .msi.

Para obter mais informações, consulte [aplicando transformações](applying-transforms.md) e [resiliência de origem](source-resiliency.md).

 

 



