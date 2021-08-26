---
description: 'Saiba mais sobre: Referência gerenciada do mecanismo Armazenamento extensível'
title: Referência gerenciada do mecanismo Armazenamento extensível
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: 38f7f09d441fa6f4158594caa8eda0b15bbe07fe909a73cd194f0886bb29914d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093676"
---
# <a name="extensible-storage-engine-managed-reference"></a>Referência gerenciada do mecanismo Armazenamento extensível

Encontre informações de referência para a biblioteca ManagedESENT. A biblioteca ManagedESENT fornece acesso gerenciado ao ESENT, o mecanismo de banco de dados inserível que é nativo do Windows.


_**Aplica-se a:** Windows | Windows Servidor_

**Neste artigo**  
Como a biblioteca ManagedESENT é diferente da ESENT?  
Requisitos  
Nesta seção  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>Como a biblioteca ManagedESENT é diferente da ESENT?

O ESENT é um mecanismo de banco de dados transacional e inserível que permite criar aplicativos personalizados que precisam de armazenamento confiável, de alto desempenho e de baixa sobrecarga de dados. O mecanismo ESENT pode ajudar com as necessidades de dados que variam de algo tão simples quanto uma tabela de hash que é muito grande para armazenar na memória, até algo mais complexo, como um aplicativo com tabelas, colunas e índices. Para criar um aplicativo com o ESENT, use a DLL esent.dll que faz parte do sistema operacional Windows e escreva seu código com C/C++. Para obter mais informações sobre o ESENT, consulte [Extensible Armazenamento Engine Reference](./extensible-storage-engine-reference.md).

O ManagedESENT é criado com base no esent.dll, que faz parte do Windows, portanto, não há binários não gerenciados adicionais para baixar e instalar. Com a biblioteca ManagedESENT, você pode criar seu aplicativo usando uma linguagem gerenciada como C em vez \# de C/C++. A biblioteca usa os mesmos nomes de tipo e membro para expor a API do ESE, portanto, se você já estiver familiarizado com a estrutura dessa API, poderá fazer a transição facilmente para essa biblioteca gerenciada.

## <a name="requirements"></a>Requisitos

Essa biblioteca gerenciada requer o seguinte:

  - Um computador executando uma versão do Windows a partir do Windows Vista

  - Visual Studio 2012

  - O .NET Framework 4.5

## <a name="in-this-section"></a>Nesta seção

  - [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
