---
description: Várias funções fornecem serviços para gerenciar um estado de armazenamento de certificados.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Gerenciando um estado de armazenamento de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cbbb41691b66abfa2d49d669b13ec7fd438bd4ae503bf944d9e4923f647f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425666"
---
# <a name="managing-a-certificate-store-state"></a>Gerenciando um estado de armazenamento de certificados

Várias funções fornecem serviços para gerenciar um estado [*de armazenamento de*](../secgloss/c-gly.md) [*certificados*](../secgloss/s-gly.md).

Para obter acesso a certificados, o repositório de certificados no qual eles são armazenados deve ser aberto por meio de uma chamada para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) ou [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).

Normalmente, um armazenamento de certificados é aberto na memória armazenada em cache. Ele pode ser um novo armazenamento ou seu conteúdo pode ser carregado do registro local, do registro em um computador remoto, de um arquivo de disco, de uma mensagem PKCS 7 ou de alguma \# outra fonte.

As funções de armazenamento de certificados CryptoAPI também permitem que um armazenamento mantenha certificados fora da memória armazenada em cache, por exemplo, em um banco de dados externo de certificados, como aquele fornecido pelo Banco de Dados do Servidor de Certificados da Microsoft.

Um dos parâmetros da função [**CertOpenStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) *lpszStoreProvider,* determina o tipo de repositório aberto e o provedor usado para abrir esse repositório. Para exemplos de abertura de armazenamentos de certificado usando vários provedores, consulte [Código C de exemplo para abrir armazenamentos de certificados](example-c-code-for-opening-certificate-stores.md).

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) fecha um repositório de certificados. Quando um armazenamento de certificados é fechado, cada um dos contextos de certificado nesse armazenamento tem sua contagem de [*referência*](../secgloss/r-gly.md) reduzida em um. A memória é liberada para certificados cuja contagem de referência vai para zero.

Definir CERT \_ CLOSE STORE FORCE FLAG com \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) fecha o repositório de certificados e libera memória para todos os seus contextos de certificado, independentemente de sua contagem de referência. Em alguns casos, como em programas multithread, isso não pode ser desejável. Se CERT CLOSE STORE CHECK FLAG estiver definido, o armazenamento será fechado, mas um valor de aviso será retornado pela função se a memória ainda estiver alocada para certificados cujas contagens de referência não foram \_ \_ \_ \_ reduzidas para zero. Se a contagem de referência de um certificado for maior que zero, uma duplicata desse contexto de certificado não será liberada. Use [**CertFreeCertificateContext,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)e [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) para liberar todos os certificados deixados abertos.

> [!Note]
> Um [*contexto de*](../secgloss/c-gly.md) certificado é uma estrutura do tipo CERT [**\_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que tem, entre outros membros, um ponteiro para o [*BLOB*](../secgloss/c-gly.md) de certificado codificado e um ponteiro para uma estrutura [**CERT \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) A **estrutura CERT \_ INFO** contém os dados de certificado mais significativos. Para obter mais informações sobre as estruturas de contexto de certificado [*,*](../secgloss/c-gly.md)CRL [*(lista*](../secgloss/c-gly.md) de certificados revogados) e CTL [*(lista*](../secgloss/c-gly.md) de confiança de certificado), consulte Codificação e [decodificação](encoding-and-decoding-a-certificate-context.md)de um contexto de certificado.
> 
> Cada contexto de certificado também contém uma contagem [*de*](../secgloss/r-gly.md) referência que indica o número de cópias do endereço do contexto que foram atribuídas. Sempre que um contexto de certificado é duplicado de qualquer forma, sua contagem de referência é incrementada em um. Sempre que um ponteiro para um contexto de certificado é liberado, a contagem de referência no contexto do certificado é decrementada por um. Quando a contagem de referência em um contexto de certificado atinge zero, a memória que mantém o contexto é desalocada. A memória alocada para um contexto de certificado também é desalocada quando esse contexto está em um armazenamento e o armazenamento é fechado usando CERT \_ CLOSE \_ STORE FORCE \_ \_ FLAG. Se a memória de um contexto for desalocada e os ponteiros para esse contexto ainda estão em uso, esses ponteiros não serão mais válidos.

 

[**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) aumenta a contagem [*de*](../secgloss/r-gly.md) referência no repositório.

[**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) salva o conteúdo de um repositório em um arquivo de disco ou em um local de memória e

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) gerencia um repositório enquanto ele está aberto. Um aplicativo com um armazenamento aberto pode ser notificado quando o estado persistente desse armazenamento é alterado por algum outro processo. Isso pode acontecer se novos certificados foram copiados para o armazenamento do computador local de um computador de controle de domínio.

Quando as alterações são descobertas, o armazenamento em cache pode sincronizar seu armazenamento em cache para corresponder ao estado persistente do armazenamento. [**O CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) também dá suporte a um processo que copia as alterações do repositório armazenado em cache para o armazenamento permanente quando essas alterações no repositório armazenado em cache não são salvas automaticamente.

Contextos de certificados parecidos com o armazenamento de certificados podem ter propriedades estendidas. [**CertSetStoreProperty adiciona**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) propriedades estendidas a um repositório de certificados. [**CertGetStoreProperty recupera**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) todas as propriedades definidas em um repositório de certificados. Atualmente, a única propriedade predefinida do armazenamento de certificados é o nome localizado de um armazenamento.

 

 
