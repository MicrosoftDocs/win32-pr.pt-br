---
description: Os aplicativos COM+ consistem em um ou mais componentes COM.
ms.assetid: e7ed2844-276e-4726-952d-e4d3be2eb6e8
title: Partes de um aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75aba454689e25e8706d4a7e3f059d498891f9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456952"
---
# <a name="parts-of-a-com-application"></a>Partes de um aplicativo COM+

Os aplicativos COM+ consistem em um ou mais componentes COM.

Os seguintes termos são usados em toda a documentação do COM+:

<dl> <dt>

<span id="COM_component"></span><span id="com_component"></span><span id="COM_COMPONENT"></span>*Componente COM*
</dt> <dd>

Uma unidade binária de código que cria objetos COM (inclui o código de empacotamento e de registro).

</dd> <dt>

<span id="COM_object"></span><span id="com_object"></span><span id="COM_OBJECT"></span>*Objeto COM*
</dt> <dd>

Uma instância de uma classe COM.

</dd> <dt>

<span id="COM_class"></span><span id="com_class"></span><span id="COM_CLASS"></span>*Classe COM*
</dt> <dd>

Uma implementação nomeada e concreta de uma ou mais interfaces. Uma classe COM é identificada por um CLSID (às vezes, por um ProgID também).

</dd> <dt>

<span id="COM_interface"></span><span id="com_interface"></span><span id="COM_INTERFACE"></span>*Interface COM*
</dt> <dd>

Um grupo de funções de método relacionadas exposto por uma classe COM que especifica um contrato. Isso inclui o nome, a assinatura da interface, a semântica da interface e o formato do buffer de marshaling. Uma interface é identificada por um IID. A sintaxe da interface é definida nas bibliotecas IDL e/ou tipo. As interfaces de uma classe COM devem ser divididas em conjuntos de métodos coesas e gerenciáveis.

Interfaces COM são imutáveis; o contrato COM indica que eles não podem ser modificados. Qualquer modificação (como adicionar métodos) requer a definição de uma nova interface.

</dd> <dt>

<span id="COM_method"></span><span id="com_method"></span><span id="COM_METHOD"></span>*Método COM*
</dt> <dd>

Um de um conjunto de funções relacionadas fornecido por uma interface COM.

</dd> </dl>

## <a name="configured-and-unconfigured-components"></a>Componentes configurados e não configurados

Para tirar proveito dos serviços que os aplicativos COM+ dão suporte, o ambiente COM+ impõe requisitos específicos em componentes COM criados para aplicativos COM+. Quando adicionado a um aplicativo COM+, um componente COM é conhecido como um *componente configurado*.

Os componentes COM criados para aplicativos COM+ são componentes de servidor em processo. O componente deve conter uma biblioteca de tipos (arquivo. tlb) para descrever todas as classes implementadas no componente e declarar as interfaces em todas as classes no componente. Você pode criar e implementar esses componentes com o Microsoft Visual Basic, Microsoft Visual C++ ou qualquer ferramenta de desenvolvimento compatível COM COM.

Um *componente não configurado* é um componente que não está instalado em um aplicativo com+. Você pode transformar a maioria dos componentes não configurados em componentes definidos simplesmente integrando-os em um aplicativo COM+.

> [!Note]  
> Não use o mesmo AppID para um aplicativo COM+ e no registro para um componente não configurado. Quando o componente não configurado é ativado, uma vez que a ativação pode recuperar as informações do aplicativo COM+ do registro que não contém as informações necessárias para a ativação COM. Problemas semelhantes podem surgir se uma chamada for feita para [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) do dllhost que hospeda o aplicativo do servidor do com+.

 

 

 
