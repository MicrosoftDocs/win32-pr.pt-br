---
description: Use tabelas de registro de módulo de mesclagem de acordo com o tipo de informações de registro.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Criando tabelas de registro do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03726481905d4efee2405d0b383f53833d840090fea74e2d41fc6ae67a8e5bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066146"
---
# <a name="authoring-merge-module-registry-tables"></a>Criando tabelas de registro do módulo de mesclagem

Use tabelas de registro de módulo de mesclagem de acordo com o tipo de informações de registro.

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a>Tabelas TypeLib, Class, AppId, ProgId, extensão, verbo ou MIME

Para bibliotecas de tipos, classes, extensões e verbos, crie informações de registro nas tabelas [TypeLib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), de [extensão](extension-table.md), [verbo](verb-table.md)ou [MIME](mime-table.md) do módulo de mesclagem. se você usar a [tabela de registro](registry-table.md) para adicionar essas informações, Windows 2000 não poderá fornecer anúncio em todo o sistema para esses componentes.

Os autores do módulo de mesclagem podem decidir não registrar usando a tabela de classes pelos seguintes motivos:

-   Para ser registrado pela tabela de classes, o arquivo deve ser o caminho Keydo seu componente. Isso pode exigir uma alteração inaceitável na organização dos componentes.
-   Uma chamada COM pode disparar uma tentativa do instalador de reinstalar uma classe anunciada. Os autores podem decidir não registrar uma classe usando a tabela de classes para evitar disparar uma reinstalação quando o computador cliente não oferecer suporte a uma interface do usuário.

## <a name="registry-table"></a>Tabela do registro

Use a tabela de registro para adicionar informações de registro que não podem ser criadas em tabelas TypeLib, Class, AppId, ProgId, extensão, verbo ou MIME. Windows 2000 não pode fornecer anúncio em todo o sistema para componentes que usam a tabela de registro.

Ao criar a tabela do registro, consulte caminhos de arquivo usando o \[ \# arquivo \] ou \[ ! \]Formato de arquivo em vez \[ de \] nome do diretório. O último formato não oferece suporte à instalação de execução da origem. O formato anterior também torna os arquivos ausentes e os componentes com falha mais fáceis de detectar.

É necessário ter cuidado ao usar texto formatado na coluna de chave da tabela de registro. como Windows Installer não reinstala componentes que já estão instalados, usar texto formatado nesse campo pode fazer com que as chaves do registro sejam deixadas para trás na remoção do aplicativo.

## <a name="selfreg-table"></a>Tabela SelfReg

Não é recomendável usar a tabela SelfReg. Para obter uma lista de motivos para não usar o auto-registro, consulte a [tabela selfreg](selfreg-table.md). Você deve usar as tabelas TypeLib, Class, AppId, ProgId, extensão, verbo e MIME sempre que possível e a tabela de registro em todos os outros casos.

 

 



