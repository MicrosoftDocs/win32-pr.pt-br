---
description: A biblioteca de registro offline é usada para modificar um hive do Registro fora do registro do sistema ativo.
ms.assetid: 61db2804-1b67-473f-8dd7-6be6c6a7184e
title: Sobre a biblioteca de registro offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c2aecf71e8e42ad96c018bb613d7aac9a4a867bb301671e9553f1768a4ce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956175"
---
# <a name="about-the-offline-registry-library"></a>Sobre a biblioteca de registro offline

A biblioteca de registro offline é usada para modificar um hive do Registro fora do registro do sistema ativo.

A biblioteca de registro offline destina-se a cenários de atualização do Registro, como manutenção de uma imagem do sistema operacional. As funções de registro offline fornecem os seguintes recursos que não estão disponíveis com as funções padrão do Registro:

-   As funções de registro offline podem ser usadas para modificar um hive do Registro em qualquer formato de registro com suporte. As funções padrão do Registro podem fazer alterações somente em um hive do Registro ativo e as alterações devem ser compatíveis com a versão do Windows em execução no sistema.
-   A biblioteca de registro offline requer apenas acesso de leitura para abrir um arquivo hive do Registro e acesso de gravação para salvar o arquivo. Nenhuma outra verificação de acesso é executada em objetos no hive, possibilitando modificar o hive com privilégios de usuário padrão. Com as funções padrão do Registro, carregar um hive no registro ativo é uma operação privilegiada que requer acesso administrativo.

As funções de registro offline não devem ser usadas como um substituto para as funções do registro do sistema pelos seguintes motivos:

-   É impossível compartilhar hives do Registro entre processos usando as funções de registro offline.
-   As funções de registro offline usam o bloqueio simples que pode levar a uma degradação de desempenho grave para aplicativos multithread.
-   As alterações feitas com as funções de registro offline não são salvas até que a [**função ORSaveHive**](orsavehive.md) seja chamada.

Os aplicativos não devem usar as funções de registro offline para ignorar os requisitos de segurança do registro do sistema. Para carregar um hive, um aplicativo em execução sem os privilégios especiais exigidos pela [função RegLoadKey](/windows/win32/api/winreg/nf-winreg-regloadkeya) pode usar a [função RegLoadAppKey.](/windows/win32/api/winreg/nf-winreg-regloadappkeya)

**Windows Server 2003 e Windows XP:** Não há suporte para a função [RegLoadAppKey.](/windows/win32/api/winreg/nf-winreg-regloadappkeya)

Um *hive de registro offline* é um hive do Registro que foi carregado na memória usando as funções de registro offline. Para criar um hive de registro offline vazio, use a [**função ORCreateHive.**](orcreatehive.md) Para modificar um hive do Registro existente, use a função [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) para salvar um hive do registro do sistema ativo em um arquivo e, em seguida, use a função [**OROpenHive**](oropenhive.md) para abrir o arquivo.

As [**funções ORCreateHive**](orcreatehive.md) e [**OROpenHive**](oropenhive.md) retornam um handle para a chave raiz do hive do Registro offline. Esse handle pode ser usado como um handle para qualquer outra chave no hive do Registro offline com as seguintes exceções: as funções [**ORCreateKey**](orcreatekey.md) e [**OROpenKey**](oropenkey.md) não podem ser usadas para retornar um alça para a chave raiz; a [**função ORCloseKey**](orclosekey.md) não pode ser usada para fechar a chave raiz; e a [**função ORDeleteKey**](ordeletekey.md) não podem ser usadas para excluir a chave raiz. Em todos esses casos, a função falha com **ERROR \_ INVALID \_ PARAMETER**.

Use a [**função ORCreateKey**](orcreatekey.md) para adicionar chaves a um hive de registro offline aberto e à [**função ORSetValue**](orsetvalue.md) para definir os valores das chaves. A biblioteca de registro offline dá suporte a outras operações básicas do Registro, como enumeração, recuperação e exclusão de chaves e valores, além de definir atributos de chave, como segurança e comportamento de virtualização. Para ver uma lista de funções, consulte [Funções de biblioteca de registro offline.](offline-registry-library-functions.md)

Para salvar as alterações feitas em um hive de registro offline aberto, use a [**função ORSaveHive**](orsavehive.md) para salvar o hive em um arquivo. (As alterações não persistem, a **menos que ORSaveHive** seja chamado.) Depois de salvar o hive, use a [**função ORCloseHive**](orclosehive.md) para fechar o hive e liberar recursos associados a ele.

Um hive de registro offline é validado somente quando ele é aberto usando a [**função OROpenHive.**](oropenhive.md) Se o hive estiver corrompido, a operação simplesmente falhará; nenhuma tentativa é feita para reparar o hive. Verificações de acesso em objetos no hive não são executadas até que o hive seja carregado em um registro ativo com a [função RegLoadKey.](/windows/win32/api/winreg/nf-winreg-regloadkeya)

As funções de registro offline não são suportadas com [as chaves predefinida.](../sysinfo/predefined-keys.md)

Todas as cadeias de caracteres de nome de chave e valor passadas para funções de registro offline devem ser Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de biblioteca de registro \_ offline](offline-registry-library-functions.md)
</dt> </dl>

 

 
