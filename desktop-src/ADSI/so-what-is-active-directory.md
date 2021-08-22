---
title: Visão geral do tutorial ADSI com Visual Basic
description: O Active Directory é um banco de dados de finalidade especial \ 8212; não é uma substituição de registro.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cd6afe11b8991b6ced53367582ddf11d8eba0ea428105d3e9ba39c625d54fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082241"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Visão geral do tutorial: ADSI com Visual Basic

> [!Note]  
> A documentação a seguir faz parte de uma descrição de cenário estendido para Visual Basic desenvolvedores. Se você estiver procurando uma visão geral do Active Directory, consulte os documentos de Pro [ti no Technet.](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)) Para obter uma análise mais detalhada do lado de desenvolvimento do Active Directory, [consulte Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Para uma introdução maior às Interfaces de Serviço do Active Directory, consulte o tópico pai deste tópico: Interfaces de Serviço do [Active Directory,](active-directory-service-interfaces-adsi.md)bem como o tópico irmão: Sobre as Interfaces de Serviço do [Active Directory.](about-adsi.md)

 

O Active Directory é um banco de dados de finalidade especial – não é uma substituição do Registro. O diretório foi projetado para lidar com um grande número de operações de leitura e pesquisa e um número significativamente menor de alterações e atualizações. Os dados do Active Directory são hierárquicos, replicados e extensíveis. Como ele é replicado, você não deseja armazenar dados dinâmicos, como preços de ações corporativas ou desempenho da CPU. Se os dados são específicos do computador, armazene os dados no Registro. Exemplos típicos de dados armazenados no diretório incluem dados de fila de impressora, dados de contato do usuário e dados de configuração de rede/computador. O banco de dados do Active Directory consiste em objetos e atributos. Objetos e definições de atributo são armazenados no esquema do Active Directory.

Você deve estar se perguntando quais objetos estão armazenados no Active Directory no momento. O Active Directory tem três partições. Eles também são conhecidos como contextos de nomentura: domínio, esquema e configuração. A partição de domínio contém usuários, grupos, contatos, computadores, unidades organizacionais e muitos outros tipos de objeto. Como o Active Directory é extensível, você também pode adicionar suas próprias classes e/ou atributos. A partição de esquema contém classes e definições de atributo. A partição de configuração inclui dados de configuração para serviços, partições e sites.

A captura de tela a seguir mostra a partição de domínio do Active Directory.

![partição de domínio do active directory](images/adadsi1.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando o Active Directory usando Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Cenário: a Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 