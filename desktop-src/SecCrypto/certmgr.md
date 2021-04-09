---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e248aef1f726b16d8f17098cfc9642393b963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091515"
---
# <a name="certmgr"></a>CertMgr

As ferramentas CertMgr substituem DumpCert. Ele inclui novos recursos para o gerenciamento de [*certificados*](../secgloss/c-gly.md), [*listas de certificados confiáveis*](../secgloss/c-gly.md) (CTLs) e [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs). A ferramenta é instalada na \\ pasta bin do caminho de instalação do SDK (Software Development Kit) do Microsoft Windows.

O CertMgr está disponível como parte do SDK do Windows, do qual você pode baixar <https://go.microsoft.com/fwlink/p/?linkid=84091> .

CertMgr executa uma das quatro funções dependendo da ação indicada no comando.

**Certmgr** \[ **-Adicionar** \| **-del** \| **-Put** \] \[  Opções \] do \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *destinationname*\]

A tabela a seguir indica as ações básicas da ferramenta CertMgr.



| Sinalizador de ação | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none        | Exibe certificados, CRLs ou CTLs. sem sinalizador de ação (para exibir somente), *SourceName* é o nome do repositório de certificados ou do arquivo que contém os itens a serem exibidos. O repositório pode ser um repositório [*serializado*](../secgloss/s-gly.md) (StoreFile) ou um repositório do sistema. Por padrão, CertMgr exibe todos os certificados, CTLs ou CRLs no repositório de certificados ou no arquivo. O *destinationname* não é usado para exibição.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -Adicionar        | Copia certificados, CTLs e CRLs para um repositório de certificados. Ao usar **-Add**, *SourceName* é o repositório de certificados de origem que contém os certificados, CTLs e CRLs existentes. *Destinationname* é o repositório de certificados de destino ao qual os certificados, CTLs e CRLs serão adicionados. O repositório de destino será salvo como um armazenamento [*serializado*](../secgloss/s-gly.md) , a menos que a opção **-7** seja usada, o que salva o repositório como um arquivo [*PKCS*](../secgloss/p-gly.md) \# 7. Observe que a opção **-7** não pode ser usada quando o repositório de destino é um repositório do sistema.<br/>                                                                                                                          |
| -del        | Exclui certificados, CTLs e CRLs de um repositório de certificados. Ao usar **-del**, *SourceName* é o repositório de certificados de origem que contém os certificados, CTLs e CRLs existentes. *Destinationname* é o repositório de certificados de destino que conterá cópias dos certificados, CTLs e CRLs restantes depois que os itens especificados tiverem sido excluídos. Se *destinationname* não for especificado, *SourceName* também funcionará como o repositório de destino (ele será modificado). O repositório de destino será salvo como um armazenamento [*serializado*](../secgloss/s-gly.md) , a menos que a opção **-7** seja usada, o que salva o repositório como um \# arquivo PKCS 7. Observe que a opção **-7** não pode ser usada quando o repositório de destino é um repositório do sistema.<br/> |
| -Put        | Salva um certificado codificado [*X. 509*](../secgloss/x-gly.md) , CTL ou CRL em um arquivo. Ao usar **-Put**, *SourceName* é o repositório de certificados de origem que contém os certificados, CTLs e CRLs existentes. *Destinationname* é o nome de um arquivo para o qual um certificado codificado [*X. 509*](../secgloss/x-gly.md) , CTL e CRL será salvo. Se a opção **-7** for usada, o arquivo será salvo como um arquivo PKCS \# 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Opções

As opções a seguir se aplicam a todas as funções CertMgr, exceto quando indicado.



| Opção                     | Sinalizador de ação                                 | Descrição                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | Nenhum (somente exibição)                         | Modo detalhado. Exibe informações detalhadas sobre certificados, CTLs e CRLs. O padrão é exibir informações resumidas.                                                                                                                       |
| **-c**                     | all                                         | Usar somente certificados.                                                                                                                                                                                                                             |
| **-CTL**                   | all                                         | Usar somente CTLs.                                                                                                                                                                                                                                     |
| **-CRL**                   | all                                         | Usar somente CRLs.                                                                                                                                                                                                                                     |
| **-todos**                   | **-Adicionar-del**<br/> **-Put**<br/> | Adiciona todas as entradas do tipo escolhido.                                                                                                                                                                                                               |
| **-e** *EncodingType*      | all                                         | [*Tipo de codificação*](../secgloss/e-gly.md)de certificado.                                                                                                                                             |
| **-y** *storeProviderType* | all                                         | Tipo de provedor de armazenamento.                                                                                                                                                                                                                               |
| **-7**                     | **-Adicionar-del**<br/> **-Put**<br/> | Salva o repositório de destino como um \# arquivo PKCS 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | all                                         | Sinalizador de armazenamento aberto. Esse é o parâmetro *dwFlags* passado para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore). O valor padrão é o \_ usuário atual do repositório do sistema de CERT \_ \_ \_ . Significativo somente se **-y** estiver definido. Para obter mais informações, consulte **CertOpenStore**.         |
| **-n** *commonNameString*  | **-Adicionar-del**<br/> **-Put**<br/> | Nome comum do certificado. Pode ser usado somente com certificados.                                                                                                                                                                                |
| **-SHA1** *sha1Hash*       | **-Adicionar-del**<br/> **-Put**<br/> | Hash SHA1 do certificado, da CTL ou da CRL a ser copiada, excluída ou salva.                                                                                                                                                                         |
| **-s**                     | all                                         | Indica que o repositório é um repositório do sistema.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | all                                         | Local do registro do repositório de certificados do sistema. Significativo somente quando **-s** é definido. Deve ser definido como *CurrentUser* (chave do registro hKey \_ Current \_ User) ou *LOCALMACHINE* (chave do registro hKey \_ local \_ Machine). *CurrentUser* é o padrão. |
| **-?**                     | all                                         | Exibe todas as opções.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O CertMgr só tem suporte no Internet Explorer 4,0 ou posterior.

CertMgr pode copiar, excluir ou salvar um ou mais certificados, CTLs ou CRLs. Se houver mais de um item em uma dessas categorias, o usuário terá três opções:

-   Use a opção **-All** para copiar, excluir ou salvar todos os itens na categoria indicada.
-   Use as opções **-n** e **-SHA1** para identificar exclusivamente o item a ser copiado, excluído ou salvo.
-   Se **-All**, ou **-n** e **-SHA1** não forem indicados, certmgr solicitará ao usuário uma lista de itens a serem copiados, excluídos ou salvos. O usuário responde inserindo o índice do item a ser copiado, excluído ou salvo.

As ações de CertMgr usam pequenas variações da sintaxe e das opções. A sintaxe e as opções específicas para uma ação devem ser usadas.

O CertMgr funciona com dois tipos de repositórios de certificados: StoreFile e repositório do sistema. Um StoreFile pode ser um dos seguintes tipos de arquivos:

-   Um arquivo CTL/CRL/certificado codificado (pode ser codificado na base 64)
-   Um \# arquivo PKCS 7
-   Um documento assinado
-   Um StoreFile serializado

Não é necessário especificar o tipo de StoreFile. CertMgr pode determinar o tipo StoreFile e executar as ações apropriadas.

Um repositório do sistema é um repositório de certificados normalmente localizado no registro em **CurrentUser**. O usuário pode se referir a um repositório do sistema fornecendo apenas seu nome. Não é necessário especificar o tipo de provedor de repositório de certificados. Dependendo do tipo de StoreFile ou do repositório do sistema, CertMgr escolhe o tipo de provedor de armazenamento correspondente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando CertMgr](using-certmgr.md)
</dt> </dl>

 

 
