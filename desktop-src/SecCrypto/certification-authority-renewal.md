---
description: Os serviços de certificados oferecem suporte à renovação de uma autoridade de certificação (CA).
ms.assetid: b6c76642-9a23-471e-af08-58e91d778f09
title: Renovação da autoridade de certificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de57cd16ae6fc4c90bfeea411a06efcb14d028b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921191"
---
# <a name="certification-authority-renewal"></a>Renovação da autoridade de certificação

Os [*serviços de certificados*](../secgloss/c-gly.md) oferecem suporte à renovação de uma autoridade de [*certificação*](../secgloss/c-gly.md) (CA). A renovação é a emissão de um novo certificado para a AC estender a vida da autoridade de certificação além da data de término de seu certificado original. Você pode renovar uma AC como uma tarefa dentro do snap-in do MMC da autoridade de certificação ou usando a ferramenta de Certutil.exe (com o comando **-renewCert** ).

Cada renovação resulta em um novo certificado de autoridade de certificação; no entanto, o administrador pode gerar um novo par de chaves públicas/privadas ou reutilizar o par de chaves pública/privada existente para o certificado de autoridade de certificação. Para consistência e integridade, os certificados de CA e as listas de certificados [*revogados*](../secgloss/c-gly.md) (CRL) emitidos pela CA antes de sua renovação estarão disponíveis depois que a AC for renovada. Para torná-los disponíveis, os serviços de certificados mantêm um índice de certificados de autoridade de certificação, CRLs e chaves.

Os índices e os nomes de sufixo de certificados de autoridade de certificação e CRLs durante várias operações de renovação de CA são os seguintes.



| Operação                | Índice de certificado de autoridade de certificação | Sufixo de nome de arquivo do certificado de autoridade de certificação | CRL e índice de chave | Sufixo de nome de contêiner de chave e CRL |
|--------------------------|----------------------|---------------------------------|-------------------|-----------------------------------|
| Instalação original da autoridade de certificação | 0                    | ""                              | 0                 | ""                                |
| Renovação com nova chave     | 1                    | "(1)"                           | 1                 | "(1)"                             |
| Renovação de reutilização de chave      | 2                    | "(2)"                           | 1                 | "(1)"                             |
| Renovação de reutilização de chave      | 3                    | "(3)"                           | 1                 | "(1)"                             |
| Renovação com nova chave     | 4                    | "(4)"                           | 4                 | "(4)"                             |
| Renovação de reutilização de chave      | 5                    | "(5)"                           | 4                 | "(4)"                             |
| Renovação com nova chave     | 6                    | "(6)"                           | 6                 | "(6)"                             |
| Renovação de reutilização de chave      | 7                    | "(7)"                           | 6                 | "(6)"                             |



 

Quando uma AC é instalada, o índice de certificado é zero e o sufixo do certificado é "" (uma cadeia de caracteres vazia). Cada vez que o certificado é renovado (quer as chaves sejam reutilizadas ou não), o índice de certificado é incrementado em um, e o sufixo do nome de arquivo do certificado se torna uma cadeia de caracteres no formato "(*n*)", em que *n* representa o número de vezes que o certificado de autoridade de certificação foi renovado. Após a primeira renovação, o índice de certificado é 1 e o sufixo de nome de arquivo de certificado é "(1)". Após a segunda renovação, o índice de certificado é 2 e o sufixo de nome de arquivo de certificado é "(2)" e assim por diante.

Embora o índice de certificado de autoridade de certificação e o sufixo sejam incrementados por um sempre que a AC for renovada, os índices de CRL e de chave e os sufixos de nome de arquivo serão definidos para o índice de certificado de autoridade de certificação somente se o processo de renovação incluir um novo par de chaves pública/privada. Se não tiver, os valores desses índices e sufixos permanecerão iguais aos do último índice. Durante a renovação, um administrador especifica se um novo par de chaves é gerado ou se o par de chaves existente é usado. (No snap-in do MMC da autoridade de certificação, uma opção na interface do usuário especifica um par de chaves novo ou existente; na ferramenta de Certutil.exe, o comando **certutil-renewCert** renova a AC com um novo par de chaves, enquanto o comando **certutil-renewCert REUSEKEYS** renova a AC com o par de chaves existente.)

O índice de CRL está diretamente vinculado ao índice de chave, que é definido para o índice de certificado de autoridade de certificação somente quando um novo par de chaves é usado para a renovação. Após a primeira renovação (que usou um novo par de chaves), o índice da CRL e da chave é definido como 1, e o sufixo do nome da CRL e do contêiner de chave é "(1)". No entanto, após a segunda renovação, o índice da CRL e da chave permanece 1, e o sufixo de nome de contêiner de chave e CRL também permanece "(1)"; Isso ocorre porque a segunda renovação usou o par de chaves existente e apenas uma CRL é emitida para cada par de chaves da autoridade de certificação.

Você pode recuperar os certificados de AC indexados e as CRLs chamando o método **Getcertificaproperty** (nas interfaces [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) e [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) ). Ao recuperar determinadas propriedades relacionadas ao certificado de autoridade de certificação ou CRL, você pode acrescentar o índice de base zero do certificado de autoridade de certificação aos nomes de propriedade. Por exemplo, para recuperar o índice de CRL que corresponde ao terceiro certificado da autoridade de certificação, passe a propriedade "CRLIndex. 2" para [**ICertServerPolicy:: Getcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty); para a tabela, o valor da propriedade "CRLIndex. 2" recuperado seria 1. Uma propriedade chamada "CertCount" pode ser usada para determinar o número de vezes que a autoridade de certificação emitiu um certificado de autoridade de certificação.

Os certificados de CA e as CRLs contêm uma extensão que fornece informações sobre o certificado e o índice de chave. A extensão é definida em Wincrypt. h como \_ \_ a versão da AC do szOID CERTSRV \_ com um valor de "1.3.6.1.4.1.311.21.1". Os dados de extensão são um valor **DWORD** (codificado como um \_ inteiro X509 na extensão); os 16 bits baixos são o índice de certificado e os 16 bits altos são o índice de chave.

A instalação inicial de uma autoridade de certificação produz um índice de certificado zero e um índice de chave igual a zero. A renovação de um certificado de autoridade de certificação fará com que o índice de certificado seja incrementado. Se a chave for reutilizada na renovação, o índice de chave será o mesmo que o índice de chave anterior. Se a chave não for reutilizada, o índice de chave corresponderá ao novo índice de certificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ICertServerPolicy:: getcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerExit:: getcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> </dl>

 

 
