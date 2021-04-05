---
title: Read-Only DCs e o esquema de Active Directory
description: O Windows Server 2008 apresenta um novo tipo de controlador de domínio, o RODC (controlador de domínio somente leitura).
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104084971"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only DCs e o esquema de Active Directory

O Windows Server 2008 apresenta um novo tipo de controlador de domínio, o RODC (controlador de domínio somente leitura). Isso fornece um controlador de domínio para uso em filiais em que um controlador de domínio completo não pode ser colocado. A intenção é permitir que os usuários nas filiais façam logon e executem tarefas como compartilhamento de arquivos/impressoras, mesmo quando não houver conectividade de rede com sites de Hub.

O RODC não altera a maneira como o esquema é usado. No entanto, vale a pena mencionar que o esquema dá suporte a um conjunto de atributos parciais Read-Only (RO-PAS), também conhecido como conjunto de atributos filtrados por RODC, que é um conjunto de atributos especiais que não é replicado para RODCs por motivos de segurança. O RO-PAS é definido no esquema por meio do atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .

## <a name="rodc-filtered-attribute-set"></a>Conjunto de atributos filtrados do RODC

Alguns aplicativos que usam [Active Directory Domain Services](active-directory-domain-services.md) como um armazenamento de dados podem ter dados como credenciais (como senhas, credenciais ou chaves de criptografia) que não devem ser armazenados em um controlador de domínio Read-Only, caso o RODC seja roubado ou comprometido. Para esse tipo de aplicativo, você pode adicionar o atributo ao conjunto de atributos filtrados do RODC para impedi-lo de replicar para RODCs na floresta e marcar o atributo como confidencial, o que remove a capacidade de ler os dados para membros do grupo de usuários autenticados (incluindo quaisquer RODCs).

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>Adicionando atributos ao conjunto de atributos filtrados do RODC

O conjunto de atributos filtrados do RODC é um conjunto dinâmico de atributos que não é replicado para nenhum RODC na floresta. Você pode configurar o conjunto de atributos filtrados do RODC em um mestre de esquema que executa o Windows Server 2008. Quando os atributos são impedidos de replicar para RODCs, esses dados não podem ser expostos desnecessariamente se um RODC é roubado ou comprometido.

Não é possível adicionar atributos críticos do sistema ao conjunto de atributos filtrados do RODC. Um atributo é crítico do sistema se for necessário para AD DS, autoridade de segurança local (LSA), Gerenciador de contas de segurança (SAM) e qualquer um dos provedores de serviços de segurança específicos da Microsoft, como o protocolo de autenticação Kerberos, para funcionar corretamente. Em versões do Windows Server 2008 após a versão beta 3, um atributo crítico do sistema tem um valor de atributo schemaFlagsEx (valor do atributo schemaFlagsEx & 0x1 = **true**).

Para obter instruções passo a passo para adicionar atributos ao conjunto de atributos filtrados do RODC, consulte [o Apêndice D do guia passo a passo para RODCs]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10)).

## <a name="marking-attributes-as-confidential"></a>Marcando atributos como confidenciais

Além disso, é recomendável que você também Marque como confidencial todos os atributos que você configurar como parte do conjunto de atributos filtrados do RODC. Para marcar um atributo como confidencial, você precisa remover a permissão de leitura para o atributo do grupo usuários autenticados. Marcar o atributo como confidencial fornece uma proteção adicional contra um RODC que é comprometido removendo as permissões necessárias para ler os dados como credenciais. Para obter mais informações sobre como marcar atributos como confidenciais, consulte [o artigo 922836 na base de dados de conhecimento Microsoft]( https://support.microsoft.com/kb/922836).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia passo a passo para controladores de domínio somente leitura]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 