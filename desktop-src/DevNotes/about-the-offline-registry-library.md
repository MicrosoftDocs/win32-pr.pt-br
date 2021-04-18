---
description: A biblioteca de registro offline é usada para modificar um hive do registro fora do registro do sistema ativo.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Sobre a biblioteca de registro offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e08b401a4a77f55a54c48ad147bf38c8796472
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456908"
---
# <a name="about-the-offline-registry-library"></a>Sobre a biblioteca de registro offline

A biblioteca de registro offline é usada para modificar um hive do registro fora do registro do sistema ativo.

A biblioteca de registro offline destina-se a cenários de atualização de registro, como manutenção de uma imagem do sistema operacional. As funções de registro offline fornecem os seguintes recursos que não estão disponíveis com as funções de registro padrão:

-   As funções de registro offline podem ser usadas para modificar um hive de registro em qualquer formato de registro com suporte. As funções de registro padrão podem fazer alterações apenas em um hive de registro ativo e as alterações devem ser compatíveis com a versão do Windows em execução no sistema.
-   A biblioteca de registro offline requer apenas acesso de leitura para abrir um arquivo do hive do registro e acesso de gravação para salvar o arquivo. Nenhuma outra verificação de acesso é executada em objetos no hive, tornando possível modificar o hive com privilégios de usuário padrão. Com as funções de registro padrão, carregar um Hive no registro ativo é uma operação privilegiada que requer acesso administrativo.

As funções de registro offline não devem ser usadas como substitutos para as funções de registro do sistema pelos seguintes motivos:

-   É impossível compartilhar hives do registro entre processos usando as funções de registro offline.
-   As funções de registro offline usam o bloqueio simples que pode levar à degradação de desempenho grave para aplicativos multissegmentados.
-   As alterações feitas com as funções de registro offline não são salvas até que a função [**ORSaveHive**](orsavehive.md) seja chamada.

Os aplicativos não devem usar as funções de registro offline para ignorar os requisitos de segurança do registro do sistema. Para carregar um Hive, um aplicativo em execução sem os privilégios especiais exigidos pela função [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) pode usar a função [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) .

**Windows Server 2003 e Windows XP:** Não há suporte para a função [RegLoadAppKey](/windows/win32/api/winreg/nf-winreg-regloadappkeya) .

Um *hive do registro offline* é um hive do registro que foi carregado na memória usando as funções do registro offline. Para criar um Hive vazio do registro offline, use a função [**ORCreateHive**](orcreatehive.md) . Para modificar um hive de registro existente, use a função [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) para salvar um hive do registro do sistema ativo em um arquivo e, em seguida, use a função [**OROpenHive**](oropenhive.md) para abrir o arquivo.

As funções [**ORCreateHive**](orcreatehive.md) e [**OROpenHive**](oropenhive.md) retornam um identificador para a chave raiz do hive do registro offline. Esse identificador pode ser usado como um identificador para qualquer outra chave no hive do registro offline com as seguintes exceções: as funções [**ORCreateKey**](orcreatekey.md) e [**OROpenKey**](oropenkey.md) não podem ser usadas para retornar um identificador para a chave raiz; a função [**ORCloseKey**](orclosekey.md) não pode ser usada para fechar a chave raiz; e a função [**ORDeleteKey**](ordeletekey.md) não pode ser usada para excluir a chave raiz. Em todos esses casos, a função falha com um **\_ \_ parâmetro de erro inválido**.

Use a função [**ORCreateKey**](orcreatekey.md) para adicionar chaves a um hive do registro offline aberto e à função [**ORSetValue**](orsetvalue.md) para definir os valores das chaves. A biblioteca de registro offline dá suporte a outras operações básicas de registro, como enumerar, recuperar e excluir chaves e valores, e definir atributos de chave como segurança e comportamento de virtualização. Para obter uma lista de funções, consulte [funções da biblioteca do registro offline](offline-registry-library-functions.md).

Para salvar as alterações feitas em um hive do registro offline aberto, use a função [**ORSaveHive**](orsavehive.md) para salvar o hive em um arquivo. (As alterações não persistim, a menos que **ORSaveHive** seja chamado.) Depois de salvar o Hive, use a função [**ORCloseHive**](orclosehive.md) para fechar o hive e liberar recursos associados a ele.

Um hive do registro offline é validado somente quando ele é aberto usando a função [**OROpenHive**](oropenhive.md) . Se o hive estiver corrompido, a operação simplesmente falhará; Não é feita nenhuma tentativa de reparar o hive. As verificações de acesso em objetos no hive não são executadas até que o hive seja carregado em um registro ativo com a função [RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) .

As funções de registro offline não dão suporte às [chaves predefinidas](../sysinfo/predefined-keys.md).

Todas as cadeias de caracteres de nome de chave e valor passadas para funções de registro offline devem ser Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções da biblioteca do registro offline \_](offline-registry-library-functions.md)
</dt> </dl>

 

 
