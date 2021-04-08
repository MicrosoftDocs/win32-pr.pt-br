---
description: 'Saiba mais sobre: referência gerenciada do mecanismo de armazenamento extensível'
title: Referência gerenciada do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010676"
---
# <a name="extensible-storage-engine-managed-reference"></a>Referência gerenciada do mecanismo de armazenamento extensível

Encontre informações de referência para a biblioteca ManagedESENT. A biblioteca ManagedESENT fornece acesso gerenciado a ESENT, o mecanismo de banco de dados incorporável que é nativo do Windows.


_**Aplica-se a:** Windows | Windows Server_

**Neste artigo**  
Como a biblioteca ManagedESENT é diferente de ESENT?  
Requisitos  
Nesta seção  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>Como a biblioteca ManagedESENT é diferente de ESENT?

O ESENT é um mecanismo de banco de dados transacional e incorporável que permite criar aplicativos personalizados que precisam de armazenamento de dados confiável, de alto desempenho e de baixa sobrecarga. O mecanismo ESENT pode ajudar com as necessidades de dados que variam de algo tão simples quanto uma tabela de hash muito grande para armazenar na memória, para algo mais complexo, como um aplicativo com tabelas, colunas e índices. Para criar um aplicativo com o ESENT, use o esent.dll DLL que faz parte do sistema operacional Windows e escreva seu código com C/C++. Para obter mais informações sobre o ESENT, consulte [referência do mecanismo de armazenamento extensível](./extensible-storage-engine-reference.md).

O ManagedESENT é criado com base em esent.dll, que faz parte do Windows, portanto, não há binários adicionais não gerenciados para baixar e instalar. Com a biblioteca ManagedESENT, você pode criar seu aplicativo usando uma linguagem gerenciada como C \# em vez de c/C++. A biblioteca usa o mesmo tipo e nomes de membros para expor a API ESE, portanto, se você já estiver familiarizado com a estrutura dessa API, poderá fazer a transição facilmente para essa biblioteca gerenciada.

## <a name="requirements"></a>Requisitos

Essa biblioteca gerenciada requer o seguinte:

  - Um computador executando uma versão do Windows a partir do Windows Vista

  - Visual Studio 2012

  - O .NET Framework 4.5

## <a name="in-this-section"></a>Nesta seção

  - [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
