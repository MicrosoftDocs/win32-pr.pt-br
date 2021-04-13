---
title: Visão geral do tutorial ADSI com Visual Basic
description: Active Directory é um banco de dados de finalidade especial \ 8212; Não é uma substituição do registro.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104554062"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>Visão geral do tutorial: ADSI com Visual Basic

> [!Note]  
> A documentação a seguir faz parte de uma descrição de cenário estendido para desenvolvedores de Visual Basic. Se você estiver procurando uma visão geral do Active Directory, consulte os [documentos profissionais de ti no TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)). Para obter uma visão mais detalhada do lado de desenvolvimento do Active Directory, consulte [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services). Para obter uma introdução maior ao Active Directory interfaces de serviço, consulte o tópico pai deste tópico: [Active Directory interfaces de serviço](active-directory-service-interfaces-adsi.md), bem como o tópico irmão: [sobre Active Directory interfaces de serviço](about-adsi.md).

 

Active Directory é um banco de dados de finalidade especial — não é uma substituição do registro. O diretório foi projetado para lidar com um grande número de operações de leitura e pesquisa e um número significativamente menor de alterações e atualizações. Active Directory dados são hierárquicos, replicados e extensíveis. Como ele é replicado, você não deseja armazenar dados dinâmicos, como preços de estoque corporativos ou desempenho da CPU. Se os dados forem específicos do computador, armazene os dados no registro. Exemplos típicos de dados armazenados no diretório incluem dados de fila da impressora, dados de contato do usuário e dados de configuração de rede/computador. O banco de dados Active Directory consiste em objetos e atributos. Os objetos e as definições de atributo são armazenados no esquema de Active Directory.

Você pode estar se perguntando quais objetos estão armazenados atualmente no Active Directory. Active Directory tem três partições. Eles também são conhecidos como contextos de nomenclatura: domínio, esquema e configuração. A partição de domínio contém usuários, grupos, contatos, computadores, unidades organizacionais e muitos outros tipos de objeto. Como Active Directory é extensível, você também pode adicionar suas próprias classes e/ou atributos. A partição de esquema contém classes e definições de atributo. A partição de configuração inclui dados de configuração para serviços, partições e sites.

A captura de tela a seguir mostra a Active Directory partição de domínio.

![partição de domínio do Active Directory](images/adadsi1.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando Active Directory usando Visual Basic](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[Cenário: a Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 