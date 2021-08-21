---
title: Read-Only DCs e o esquema do Active Directory
description: Windows O Servidor 2008 apresenta um novo tipo de controlador de domínio, o RODC (Controlador de Domínio Somente Leitura).
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9616230c38ad3d210aca5e18d5492a09610b9b3048b72f810c3c0ac466c4ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184147"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only DCs e o esquema do Active Directory

Windows O Servidor 2008 apresenta um novo tipo de controlador de domínio, o RODC (Controlador de Domínio Somente Leitura). Isso fornece um controlador de domínio para uso em filiais em que um controlador de domínio completo não pode ser colocado. A intenção é permitir que os usuários nas filiais faça logon e executem tarefas como compartilhamento de arquivos/impressoras, mesmo quando não há conectividade de rede com sites de hub.

RODC não altera a maneira como o esquema é usado. No entanto, vale a pena mencionar que o esquema dá suporte a um RO-PAS (Conjunto de Atributos Parciais) do Read-Only, também conhecido como conjunto de atributos filtrados rodc, que é um conjunto de atributos especial QUE NÃO é replicado para RODCs por motivos de segurança. RO-PAS são definidos no esquema por meio do [**atributo searchFlags.**](/windows/desktop/ADSchema/a-searchflags)

## <a name="rodc-filtered-attribute-set"></a>Conjunto de atributos filtrados rodc

Alguns aplicativos que usam [Active Directory Domain Services](active-directory-domain-services.md) como um armazenamento de dados podem ter dados como credenciais (como senhas, credenciais ou chaves de criptografia) que não devem ser armazenados em um controlador de domínio do Read-Only caso o RODC seja roubado ou comprometido. Para esse tipo de aplicativo, você pode adicionar o atributo ao conjunto de atributos filtrados rodc para impedir que ele seja replicado para RODCs na floresta e marcar o atributo como confidencial, o que remove a capacidade de ler os dados de membros do grupo Usuários Autenticados (incluindo quaisquer RODCs).

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>Adicionando atributos ao conjunto de atributos filtrados rodc

O conjunto de atributos filtrados rodc é um conjunto dinâmico de atributos que não é replicado para nenhum RODCs na floresta. Você pode configurar o conjunto de atributos filtrados rodc em um mestre de esquema que executa Windows Server 2008. Quando os atributos são impedidos de replicar em RODCs, esses dados não poderão ser expostos desnecessariamente se um RODC for roubado ou comprometido.

Não é possível adicionar atributos críticos do sistema ao conjunto de atributos filtrados rodc. Um atributo será crítico para o sistema se for necessário para que AD DS, LSA (Autoridade de Segurança Local), SAM (Gerenciador de Contas de Segurança) e qualquer um dos Provedores de Serviços de Segurança específicos da Microsoft, como o protocolo de autenticação Kerberos, funcionem corretamente. Em versões do Windows Server 2008 após a Beta 3, um atributo crítico do sistema tem um valor de atributo schemaFlagsEx de (valor do atributo schemaFlagsEx & 0x1 = **TRUE**).

Para obter instruções passo a passo sobre como adicionar atributos ao conjunto de atributos filtrados rodc, consulte o Apêndice D do guia passo a passo [para RODCs]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10)).

## <a name="marking-attributes-as-confidential"></a>Marcando atributos como confidenciais

Além disso, é recomendável que você também marque como confidencial todos os atributos que você configurar como parte do conjunto de atributos filtrados rodc. Para marcar um atributo confidencial, você precisa remover a permissão Leitura do atributo para o grupo Usuários Autenticados. Marcar o atributo como confidencial fornece uma proteção adicional contra um RODC comprometido removendo as permissões necessárias para ler os dados como credenciais. Para obter mais informações sobre como marcar atributos como confidenciais, consulte [o artigo 922836 no Base de Dados de Conhecimento Microsoft]( https://support.microsoft.com/kb/922836).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia passo a passo para controladores de domínio somente leitura]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 