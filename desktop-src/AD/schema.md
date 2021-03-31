---
title: Esquema (AD DS)
description: Active Directory esquema é implementado como um conjunto de instâncias de classe de objeto armazenadas no diretório.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory de esquema de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "103639030"
---
# <a name="schema-ad-ds"></a>Esquema (AD DS)

Active Directory esquema é implementado como um conjunto de instâncias de classe de objeto armazenadas no diretório. Isso é muito diferente de muitos diretórios que têm um esquema, mas os armazenam como um arquivo de texto lido na inicialização. O armazenamento do esquema no diretório tem muitas vantagens. Por exemplo, os aplicativos de usuário podem lê-lo para descobrir quais objetos e propriedades estão disponíveis.

Active Directory esquema pode ser atualizado dinamicamente. Ou seja, um aplicativo pode estender o esquema com novos atributos e classes e usar as extensões imediatamente. As atualizações de esquema são realizadas criando ou modificando os objetos de esquema armazenados no diretório. Como todos os objetos em Active Directory, ACLs (listas de controle de acesso) protegem objetos de esquema, para que os usuários autorizados só possam alterar o esquema.

Para obter mais informações, consulte [Active Directory esquema](active-directory-schema.md).

 

 




