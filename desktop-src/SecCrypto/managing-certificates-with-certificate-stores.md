---
description: Usar funções de CryptoAPI para gerenciar repositórios de certificados e certificados, listas de certificados revogados e listas de certificados confiáveis nessas lojas.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Gerenciando certificados com repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570966"
---
# <a name="managing-certificates-with-certificate-stores"></a>Gerenciando certificados com repositórios de certificados

Durante um período de tempo, os [*certificados*](../secgloss/c-gly.md) serão acumulados no computador de um usuário. As ferramentas são necessárias para gerenciar esses certificados. O [*CryptoAPI*](../secgloss/c-gly.md) fornece essas ferramentas como funções para armazenar, recuperar, excluir, listar (enumerar) e verificar certificados. O CryptoAPI também fornece os meios para anexar certificados a mensagens.

A CryptoAPI oferece duas categorias principais de funções para gerenciar certificados: funções que gerenciam [*repositórios de certificados*](../secgloss/c-gly.md)e funções que funcionam com certificados, CRLs ( [*listas de certificados revogados*](../secgloss/c-gly.md) ) e [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) nesses armazenamentos.

As funções que gerenciam os [*repositórios de certificados*](../secgloss/c-gly.md) incluem funções para trabalhar com [*repositórios*](../secgloss/v-gly.md)lógicos ou virtuais, [*repositórios remotos*](../secgloss/r-gly.md), [*repositórios externos*](../secgloss/e-gly.md)e repositórios que podem ser realocados.

Certificados, [*CRLs*](../secgloss/c-gly.md)e [*CTLs*](../secgloss/c-gly.md) podem ser mantidos e mantidos em [*repositórios de certificados*](../secgloss/c-gly.md). Eles podem ser recuperados de uma loja em que foram persistidos para uso em processos de autenticação.

O [*repositório de certificados*](../secgloss/c-gly.md) é fundamental para toda a funcionalidade de certificado. Os certificados são gerenciados no armazenamento usando funções com um prefixo "CERT". Um repositório de certificados típico é uma lista vinculada de [*certificados*](../secgloss/c-gly.md) , conforme mostrado na ilustração a seguir.

![repositório de certificados](images/certstore1.png)

A ilustração anterior mostra:

-   Cada [*repositório de certificados*](../secgloss/c-gly.md) tem um ponteiro para o primeiro bloco de certificado nesse armazenamento.
-   Um bloco de certificado inclui um ponteiro para os dados desse certificado e um ponteiro "próximo" para o próximo bloco de certificado no repositório.
-   O ponteiro "Next" no último bloco de certificado é definido como **NULL**.
-   O bloco de dados de um certificado contém o contexto de certificado somente leitura e todas as propriedades estendidas do certificado.
-   O bloco de dados de cada certificado contém uma [*contagem de referência*](../secgloss/r-gly.md) que controla o número de ponteiros para o certificado existente.

Os certificados em um [*repositório de certificados*](../secgloss/c-gly.md) normalmente são mantidos em algum tipo de armazenamento permanente, como um arquivo de disco ou o registro do sistema. Os repositórios de certificados também podem ser criados e abertos estritamente na memória. Um armazenamento de memória fornece armazenamento de certificado temporário para trabalhar com certificados que não precisam ser mantidos.

Locais de armazenamento adicionais permitem que as lojas sejam mantidas e pesquisadas em várias partes do registro de um computador local ou, com as permissões adequadas definidas, no registro em um computador remoto.

Cada usuário tem uma minha loja pessoal na qual os certificados desse usuário estão armazenados. O meu repositório pode estar em qualquer um dos vários locais físicos, incluindo o registro em um computador local ou remoto, um arquivo de disco, um banco de dados, um serviço de diretório, um [*cartão inteligente*](../secgloss/s-gly.md)ou outro local. Embora qualquer certificado possa ser armazenado no meu repositório, esse armazenamento deve ser reservado para os certificados pessoais de um usuário: os certificados usados para assinar e descriptografar as mensagens desse usuário.

O uso de certificados para autenticação depende de ter certificados emitidos por algum emissor de certificado confiável. Certificados para emissores de certificados confiáveis normalmente são mantidos no armazenamento raiz, que é persistido atualmente em uma subchave do registro. No contexto de CryptoAPI, o armazenamento raiz é protegido e as caixas de diálogo da interface do usuário lembram o usuário para posicionar apenas os certificados confiáveis nesse armazenamento. Em situações de rede corporativa, os certificados podem ser enviados por push (copiados) por um administrador do sistema do computador do controlador de domínio para os armazenamentos raiz em computadores cliente. Esse processo fornece todos os membros de um domínio com listas de confiança semelhantes.

Outros certificados podem ser armazenados no repositório do sistema de [*autoridade de certificação*](../secgloss/c-gly.md) (CA) ou em armazenamentos baseados em arquivo, criados pelo usuário.

Para obter listas de funções para usar e manter repositórios de certificados, consulte [funções de repositório de certificados](cryptography-functions.md).

Para obter um exemplo que usa algumas dessas funções, consulte [exemplo C programa: operações de repositório de certificados](example-c-program-certificate-store-operations.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando um estado de repositório de certificados](managing-a-certificate-store-state.md)
</dt> <dt>

[Trabalhando com certificados em repositórios de certificados](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[Links de certificado](certificate-links.md)
</dt> <dt>

[Repositórios de coleta](collection-stores.md)
</dt> <dt>

[Repositórios lógicos e físicos](logical-and-physical-stores.md)
</dt> <dt>

[Locais de armazenamento do sistema](system-store-locations.md)
</dt> <dt>

[Migração do repositório de certificados](certificate-store-migration.md)
</dt> </dl>

 

 
