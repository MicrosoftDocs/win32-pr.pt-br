---
description: A finalidade do invólucro do fornecedor é encapsular e usar as interfaces COM de baixo nível (fornecidas pelos fabricantes de cartão inteligente) para um cartão inteligente específico. Essas interfaces não são fornecidas pela Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Provedor de serviços de wrapper de fornecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeec4a8a5125e8fe19201a6c810eb87705eb7b5614b49fb455e8a96af63c8d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785836"
---
# <a name="vendor-wrapper-service-provider"></a>Provedor de serviços de wrapper de fornecedor

A finalidade do invólucro do fornecedor é encapsular e usar as interfaces COM de baixo nível (fornecidas pelos fabricantes de cartão inteligente) para um cartão inteligente específico. Essas interfaces não são fornecidas pela Microsoft.

![invólucro do fornecedor](images/scspart1.png)

Conforme descrito na parte 6 da *especificação de interoperabilidade para ICCs e sistemas de computadores pessoais* (consulte [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) as especificações em), a funcionalidade exposta por esse wrapper é mais fácil de usar do que a funcionalidade de quatro provedores de serviços separados. A funcionalidade do wrapper pode ser dividida em quatro áreas principais:

-   Serviços de autenticação de cartão inteligente, como obter desafio e autenticação de cartão.
-   Acesso a arquivos de cartão inteligente ou serviços do sistema de arquivos, como abrir, fechar, ler e gravar.
-   Gerenciamento de cartão inteligente, como anexar e desanexar.
-   Serviços de verificação de cartão inteligente, como verificar e alterar código.

> [!Note]  
> Essa especificação pode não estar disponível em alguns idiomas e países ou regiões.

 

A funcionalidade é específica para o tipo de cartão que está sendo usado (que funções o cartão dá suporte, protocolos e assim por diante) e será diferente para cada cartão.

O wrapper de exemplo do Microsoft SCardCOM usa a biblioteca COM ATL para implementar um wrapper simples e criar um modelo para outros wrappers. Ele implementa as seguintes interfaces.



| Interface ou objeto                                     | Descrição                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Serviços de autenticação.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Serviços do sistema de arquivos.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Serviços de gerenciamento.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Serviços de verificação.<br/>   |



 

> [!Note]  
> O exemplo de SCardCOM é fornecido apenas como um exemplo de implementação das interfaces de wrapper. Para evitar a colisão de nome de DLL com outros fornecedores, você não deve usar SCardCOM.dll como o nome de qualquer DLL que você criar.

 

A seguir está um uso típico do wrapper do fornecedor. Este exemplo usa a interface [**ISCardManage**](iscardmanage.md) para criar instâncias das interfaces que serão encapsuladas no provedor de serviços e na interface [**ISCardVerify**](iscardverify.md) para verificar sua operação.

**Para criar um provedor de serviços de wrapper**

1.  Crie uma instância da interface [**ISCardManage**](iscardmanage.md) . Use essa interface para criar uma instância de interfaces necessárias (por exemplo, [**ISCardFileAccess**](iscardfileaccess.md) ou [**ISCardVerify**](iscardverify.md)). Ao criar essas interfaces, todas as interfaces COM de baixo nível correspondentes também seriam criadas.
2.  Anexe/Conecte-se a um cartão por meio do método [**ISCardManage**](iscardmanage.md) apropriado.
3.  Execute as operações necessárias por meio do método [**ISCardVerify**](iscardverify.md) apropriado (que pode chamar várias interfaces com de baixo nível e métodos para concluir).
4.  Repita para outras operações.
5.  Liberar ao concluir.

O nome da interface COM e o identificador de interface (GUID) não devem ser alterados dos usados no código ou no wrapper de exemplo. No entanto, o GUID de classe (ou seja, onde uma implementação real de uma interface reside) deve ser alterado daqueles usados. Isso é especialmente importante ao implementar um wrapper de fornecedor. Um exemplo seria usar vários wrappers de fornecedor em um computador específico. Esses wrappers devem implementar as mesmas interfaces COM, mas sempre usarão estratégias de implementação diferentes. Portanto, classes diferentes (e IDs de classe) são necessárias.

 

 




