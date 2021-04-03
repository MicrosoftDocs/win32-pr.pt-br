---
description: Várias funções fornecem serviços para gerenciar um estado de repositório de certificados.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Gerenciando um estado de repositório de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d66e40817f0f92f48e8841455998eff4dbffd6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930232"
---
# <a name="managing-a-certificate-store-state"></a>Gerenciando um estado de repositório de certificados

Várias funções fornecem serviços para gerenciar um [](../secgloss/c-gly.md) [*estado*](../secgloss/s-gly.md)de repositório de certificados.

Para obter acesso a certificados, o repositório de certificados no qual eles são armazenados deve ser aberto por meio de uma chamada para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) ou [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).

Geralmente, um repositório de certificados é aberto na memória armazenada em cache. Pode ser um novo repositório ou seu conteúdo pode ser carregado do Registro local, do registro em um computador remoto, de um arquivo de disco, de uma \# mensagem PKCS 7 ou de alguma outra fonte.

As funções de repositório de certificados CryptoAPI também permitem que um armazenamento mantenha certificados fora da memória armazenada em cache, por exemplo, um banco de dados externo de certificados, como o fornecido pelo banco de dados do Microsoft Certificate Server.

Um dos parâmetros da função [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) , *lpszStoreProvider,* determina o tipo de armazenamento aberto e o provedor usado para abrir esse armazenamento. Para obter exemplos de como abrir armazenamentos de certificados usando vários provedores, consulte o [código C de exemplo para abrir repositórios de certificados](example-c-code-for-opening-certificate-stores.md).

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) fecha um repositório de certificados. Quando um repositório de certificados é fechado, cada um dos contextos de certificado nesse repositório tem sua [*contagem de referência*](../secgloss/r-gly.md) reduzida em um. A memória é liberada para certificados cuja contagem de referência vai para zero.

A configuração \_ \_ \_ do sinalizador de forçar repositório de fechamento de certificado \_ com [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) fecha o repositório de certificados e libera memória para todos os seus contextos de certificado, independentemente de sua contagem de referência. Em alguns casos, como em programas multissegmentados, isso não pode ser desejável. Se \_ \_ \_ \_ o sinalizador de verificação do repositório fechar o certificado estiver definido, o repositório será fechado, mas um valor de aviso será retornado pela função se a memória ainda estiver alocada para certificados cujas contagens de referência não foram reduzidas para zero. Se a contagem de referência de um certificado for maior que zero, uma duplicata desse contexto de certificado não foi liberada. Use [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)e [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) para liberar quaisquer certificados deixados abertos.

> [!Note]
> Um [*contexto de certificado*](../secgloss/c-gly.md) é uma estrutura do tipo de [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado que tem, entre outros membros, um ponteiro para o [*blob de certificado*](../secgloss/c-gly.md) codificado e um ponteiro para uma estrutura de [**\_ informações de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) . A estrutura de **\_ informações de certificado** contém os dados de certificado mais significativos. Para obter mais informações sobre [*certificados*](../secgloss/c-gly.md), CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) e estruturas de contexto de CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ), consulte [codificar e decodificar um contexto de certificado](encoding-and-decoding-a-certificate-context.md).
> 
> Cada contexto de certificado também contém uma [*contagem de referência*](../secgloss/r-gly.md) indicando o número de cópias do endereço do contexto que foram atribuídas. Cada vez que um contexto de certificado é duplicado de qualquer forma, sua contagem de referência é incrementada em um. Cada vez que um ponteiro para um contexto de certificado é liberado, a contagem de referência no contexto de certificado é decrementada por um. Quando a contagem de referência em um contexto de certificado chega a zero, a memória que contém o contexto é desalocada. A memória alocada para um contexto de certificado também é desalocada quando esse contexto está em um repositório e o repositório é fechado usando o sinalizador de força de armazenamento de fechamento de certificado \_ \_ \_ \_ . Se a memória de um contexto for desalocada e os ponteiros para esse contexto ainda estiverem em uso, esses ponteiros não serão mais válidos.

 

[**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) aumenta a [*contagem de referência*](../secgloss/r-gly.md) na loja.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) salva o conteúdo de um repositório em um arquivo de disco ou um local de memória, e

O [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) gerencia um repositório enquanto ele está aberto. Um aplicativo com um armazenamento aberto pode ser notificado quando o estado persistente desse armazenamento tiver sido alterado por algum outro processo. Isso pode acontecer se novos certificados fossem copiados para o repositório do computador local de um computador de controle de domínio.

Quando as alterações são descobertas, o armazenamento em cache pode sincronizar novamente seu armazenamento armazenado em cache para corresponder ao estado persistente do repositório. O [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) também dá suporte a um processo que copia as alterações de armazenamento em cache para o armazenamento permanente quando essas alterações no armazenamento em cache não são salvas automaticamente.

Os contextos de certificado semelhantes ao repositório de certificados podem ter propriedades estendidas. [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) adiciona propriedades estendidas a um repositório de certificados. [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) recupera todas as propriedades definidas em um repositório de certificados. Atualmente, a única propriedade de repositório de certificados predefinida é o nome localizado de um repositório.

 

 
