---
title: Criando e mantendo um ponto de conexão de serviço
description: Ao publicar com um SCP, lembre-se de que ele deve conter dados atuais sobre a instância do serviço.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Criando e mantendo um anúncio de ponto de conexão de serviço
- ponto de conexão de serviço AD, criando e mantendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007337"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a>Criando e mantendo um ponto de conexão de serviço

Ao publicar com um SCP, lembre-se de que ele deve conter dados atuais sobre a instância do serviço. Caso contrário, os clientes que se associam ao SCP recuperam dados desatualizados. Seu instalador de serviço, que cria um SCP, especifica os valores iniciais para os atributos SCPs. Em seguida, quando a instância do serviço é iniciada, ela deve localizar o SCP e atualizar os valores de atributo, se necessário. Dessa forma, os clientes estão garantidos os dados mais atuais.

Depois de criar o SCP, seu instalador de serviço executa duas etapas adicionais que permitem que seu serviço atualize o SCP:

-   Defina ACEs no descritor de segurança do objeto SCP para permitir que o serviço modifique os atributos do SCP em tempo de execução. Para obter mais informações e um exemplo de código, consulte [habilitando a conta de serviço para acessar as propriedades do SCP](enabling-service-account-to-access-scp-properties.md).
-   Armazene o **objectGUID** do SCP no registro no computador host do serviço. O serviço recupera o GUID armazenado em cache para associar ao SCP para verificar e atualizar seus atributos.

O instalador do serviço armazena em cache o **objectGUID** do SCP em vez de seu DN. O **objectGUID** nunca muda, independentemente de o SCP ser movido ou renomeado. O DN pode ser alterado se um administrador mover ou renomear o SCP. Por exemplo, se você criar um SCP como um filho de um objeto de computador, o nome distinto do SCP será alterado se o computador for renomeado ou movido para um domínio ou unidade organizacional diferente.

Quando um instalador do serviço cria um SCP, ele deve ler o **objectGUID** do objeto recém-criado e armazená-lo no registro do computador host do serviço. Use o método [**IADs:: get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) para obter o valor **objectGUID** no formato de cadeia de caracteres adequado para associação. Armazene a cadeia de caracteres GUID como um valor na seguinte chave do registro.

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

Em que "nome do fornecedor" e "nome do produto" identificam o fornecedor e o produto.

Quando o serviço é iniciado, ele recupera a cadeia de caracteres GUID armazenada em cache do registro e a usa para associar ao SCP. O serviço lê os atributos de SCP importantes e os compara com os valores atuais. Se os valores de SCP estiverem desatualizados, o serviço os atualizará. Os valores que o serviço pode exigir para atualizar incluem **palavras-chave**, **ServiceBindingInformation**, **serviceDNSName** e **serviceDNSNameType**.

## <a name="examples"></a>Exemplos

-   [Exemplos de script](script-samples-for-managing-service-connection-points.md)
-   [Exemplos de código (C/C++)](code-samples-for-managing-service-connection-points.md)

 

 