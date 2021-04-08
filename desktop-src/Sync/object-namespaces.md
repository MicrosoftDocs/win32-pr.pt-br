---
description: Um namespace de objeto protege objetos nomeados contra acesso não autorizado.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Namespaces de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3eed750bc91c128251cc66fd7f9ed167771150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828535"
---
# <a name="object-namespaces"></a>Namespaces de objeto

Um *namespace de objeto* protege objetos nomeados contra acesso não autorizado. A criação de um namespace privado permite que aplicativos e serviços criem um ambiente mais seguro.

Um processo pode criar um namespace privado usando a função [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) . Essa função requer que você especifique um *limite* que define como os objetos no namespace devem ser isolados. O chamador deve estar dentro do limite especificado para que a operação de criação tenha sucesso. Para especificar um limite, use as funções [**CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) e [**AddSIDToBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor) .

O parâmetro *lpAliasPrefix* de [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) serve como o nome do namespace. Cada namespace é identificado exclusivamente pelo seu nome e limites. O sistema dá suporte a vários namespaces privados com o mesmo nome, desde que especifique limites diferentes.

Suponha que um processo solicite a criação de um namespace, NS1, que define um limite que contém dois elementos: o SID do administrador e o número da sessão atual. O namespace será criado se o processo estiver sendo executado sob a conta de administrador na sessão especificada. Outro processo pode acessar esse namespace usando a função [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) . O nome e o limite especificados devem corresponder se esse processo for abrir o namespace criado pelo primeiro processo. Observe que um processo pode abrir um namespace existente mesmo se ele não estiver dentro do limite, a menos que o criador tenha acesso restrito ao namespace usando o parâmetro *lpPrivateNamespaceAttributes* .

Os objetos criados nesse namespace têm nomes que são do *prefixo* de formulário \\ *objectname*. O prefixo é o nome do namespace especificado pelo parâmetro *lpAliasPrefix* de [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea). Por exemplo, para criar um objeto de evento chamado MyEvent no namespace NS1, chame a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) com o parâmetro *LPNAME* definido como ns1 \\ MyEvent.

O processo que criou o namespace pode usar a função [**ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) para fechar o identificador para o namespace. O identificador também é fechado quando o processo que criou o namespace é encerrado. Depois que o identificador do namespace for fechado, as chamadas subsequentes para [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) falharão, mas todas as operações em objetos no namespace serão realizadas com êxito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Namespaces de objeto kernel](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
