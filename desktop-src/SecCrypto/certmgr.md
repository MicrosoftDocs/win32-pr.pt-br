---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832610510eeb74b821ec690cab93fd9af74d69ca3479508b5c0707d45f491c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769985"
---
# <a name="certmgr"></a>CertMgr

As ferramentas certMgr substituem DumpCert. Ele inclui novos recursos para o gerenciamento de [*certificados,*](../secgloss/c-gly.md)CTLs [*(listas*](../secgloss/c-gly.md) de confiança de certificado) e CRLs [*(listas*](../secgloss/c-gly.md) de certificados revogados). A ferramenta é instalada na pasta Bin do caminho de instalação do \\ SDK (Software Development Kit) do Microsoft Windows.

O CertMgr está disponível como parte do Windows SDK, que você pode baixar do <https://go.microsoft.com/fwlink/p/?linkid=84091> .

O CertMgr executa uma das quatro funções, dependendo da ação indicada no comando.

**CertMgr** \[ **-add** \| **-del** \| **-put** \] \[  \] Opções \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *DestinationName*\]

A tabela a seguir indica as ações básicas da ferramenta CertMgr.



| Sinalizador de ação | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nenhum        | Exibe certificados, CRLs ou CTLs. Sem nenhum sinalizador de ação (para exibir apenas), *SourceName* é o nome do arquivo ou do armazenamento de certificados que contém os itens a exibir. O armazenamento pode ser [*um armazenamento serializado*](../secgloss/s-gly.md) (StoreFile) ou um armazenamento do sistema. Por padrão, o CertMgr exibe todos os certificados, CTLs ou CRLs no arquivo ou no armazenamento de certificados. *DestinationName* não é usado para exibição.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -add        | Copia certificados, CTLs e CRLs para um armazenamento de certificados. Ao usar **-add**, *SourceName* é o armazenamento de certificados de origem que contém os certificados, CTLs e CRLs existentes. *DestinationName* é o armazenamento de certificados de destino ao qual os certificados, CTLs e CRLs serão adicionados. O armazenamento de destino será salvo como um armazenamento [*serializado,*](../secgloss/s-gly.md) a menos que a opção **-7** seja usada, o que salva o armazenamento como um [*arquivo PKCS*](../secgloss/p-gly.md) \# 7. Observe que a **opção -7** não pode ser usada quando o armazenamento de destino é um armazenamento do sistema.<br/>                                                                                                                          |
| -del        | Exclui certificados, CTLs e CRLs de um armazenamento de certificados. Ao usar **-del**, *SourceName* é o armazenamento de certificados de origem que contém os certificados, CTLs e CRLs existentes. *DestinationName* é o armazenamento de certificados de destino que conterá cópias dos certificados, CTLs e CRLs restantes depois que os itens especificados foram excluídos. Se *DestinationName* não for especificado, *SourceName* também servirá como o armazenamento de destino (ele será modificado). O armazenamento de destino será salvo como um armazenamento [*serializado,*](../secgloss/s-gly.md) a menos que a opção **-7** seja usada, o que salva o armazenamento como um arquivo PKCS \# 7. Observe que a **opção -7** não pode ser usada quando o armazenamento de destino é um armazenamento do sistema.<br/> |
| -put        | Salva um [*certificado codificado em X.509,*](../secgloss/x-gly.md) CTL ou CRL em um arquivo. Ao usar **-put,** *SourceName* é o armazenamento de certificados de origem que contém os certificados, CTLs e CRLs existentes. *DestinationName* é o nome de um arquivo no qual um certificado codificado em [*X.509,*](../secgloss/x-gly.md) CTL e CRL será salvo. Se a **opção -7** for usada, o arquivo será salvo como um arquivo PKCS \# 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Opções

As opções a seguir se aplicam a todas as funções certMgr, exceto quando anotou.



| Opção                     | Sinalizador de ação                                 | Descrição                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | none (somente exibição)                         | Modo detalhado. Exibe informações detalhadas sobre certificados, CTLs e CRLs. O padrão é exibir informações breves.                                                                                                                       |
| **-c**                     | all                                         | Use apenas certificados.                                                                                                                                                                                                                             |
| **-CTL**                   | all                                         | Use somente CTLs.                                                                                                                                                                                                                                     |
| **-CRL**                   | all                                         | Use somente CRLs.                                                                                                                                                                                                                                     |
| **-all**                   | **-add-del**<br/> **-put**<br/> | Adiciona todas as entradas do tipo escolhido.                                                                                                                                                                                                               |
|  *-encodingType*      | all                                         | Tipo [*de codificação de certificado*](../secgloss/e-gly.md).                                                                                                                                             |
| **-y** *storeProviderType* | all                                         | Tipo de provedor de armazenamento.                                                                                                                                                                                                                               |
| **-7**                     | **-add-del**<br/> **-put**<br/> | Salva o armazenamento de destino como um arquivo PKCS \# 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | all                                         | Armazenar sinalizador aberto. Esse é o *parâmetro dwFlags* passado [**para CertOpenStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) O valor padrão é CERT \_ SYSTEM \_ STORE CURRENT \_ \_ USER. Significativo somente se **-y** estiver definido. Para obter mais informações, **consulte CertOpenStore**.         |
| **-n** *commonNameString*  | **-add-del**<br/> **-put**<br/> | Nome comum do certificado. Pode ser usado somente com certificados.                                                                                                                                                                                |
| **-sha1** *sha1Hash*       | **-add-del**<br/> **-put**<br/> | Hash SHA1 do certificado, CTL ou CRL a ser copiado, excluído ou salvo.                                                                                                                                                                         |
| **-s**                     | all                                         | Indica que o armazenamento é um armazenamento do sistema.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | all                                         | Local do Registro do armazenamento de certificados do sistema. Significativo somente quando **-s** está definido. Deve ser definido como *currentUser* (chave do Registro HKEY CURRENT USER) ou \_ \_ *localMachine* (chave do Registro HKEY \_ LOCAL \_ MACHINE). *currentUser* é o padrão. |
| **-?**                     | all                                         | Exibe todas as opções.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

O CertMgr só tem suporte no Internet Explorer 4.0 ou posterior.

O CertMgr pode copiar, excluir ou salvar um ou mais certificados, CTLs ou CRLs. Se houver mais de um item em uma dessas categorias, o usuário terá três opções:

-   Use a **opção -all** para copiar, excluir ou salvar todos os itens na categoria indicada.
-   Use as **opções -n** e **-sha1** para identificar exclusivamente o item a ser copiado, excluído ou salvo.
-   Se **-all** ou **-n** e **-sha1** não são indicados, o CertMgr solicita ao usuário uma lista de itens a copiar, excluir ou salvar. O usuário responde inserindo o índice do item a ser copiado, excluído ou salvo.

As ações do CertMgr usam pequenas variações da sintaxe e das opções. A sintaxe e as opções específicas de uma ação devem ser usadas.

O CertMgr funciona com dois tipos de armazenamentos de certificados: StoreFile e armazenamento do sistema. Um StoreFile pode ser um dos seguintes tipos de arquivos:

-   Um arquivo CTL/CRL/certificado codificado (pode ser codificado em base 64)
-   Um arquivo PKCS \# 7
-   Um documento assinado
-   Um StoreFile serializado

Não é necessário especificar o tipo do StoreFile. O CertMgr pode determinar o tipo StoreFile e tomar as ações apropriadas.

Um armazenamento do sistema é um armazenamento de certificados normalmente localizado no Registro **em currentUser.** O usuário pode se referir a um armazenamento do sistema fornecendo apenas seu nome. Não é necessário especificar o tipo de provedor de armazenamento de certificados. Dependendo do tipo de StoreFile ou do armazenamento do sistema, o CertMgr escolhe o tipo de provedor de lojas correspondente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando CertMgr](using-certmgr.md)
</dt> </dl>

 

 
