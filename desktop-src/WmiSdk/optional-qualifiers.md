---
description: Qualificadores opcionais abordam situações recorrentes não comuns a todas as implementações em conformidade com CIM, que não são necessárias para interpretar esses qualificadores.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Qualificadores opcionais
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05cd80cbccf2c67baaeac2982c896a0c74ead227619bfb17517a039fadf24a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050534"
---
# <a name="optional-qualifiers"></a>Qualificadores opcionais

Qualificadores opcionais abordam situações recorrentes não comuns a todas as implementações em conformidade com CIM, que não são necessárias para interpretar esses qualificadores. Os qualificadores opcionais são fornecidos na especificação para evitar qualificadores aleatórios definidos pelo usuário que podem ocorrer nessas situações recorrentes.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Apagar**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: associações, referências

Para associações, indica se a associação qualificada deve ser excluída se qualquer um dos objetos referenciados na associação for excluído e se o respectivo objeto referenciado na associação for qualificado com **IfDeleted**. O padrão é **false**.

Para referências, esse qualificador indica se o objeto referenciado deve ser excluído se a associação que contém a referência for excluída e qualificada com **IfDeleted**, ou se qualquer um dos objetos referenciados na associação for excluído e o respectivo objeto referenciado na associação for qualificado com **IfDeleted**.

Uso: os aplicativos devem controlar associações e referências marcadas com o qualificador de **exclusão** e excluir a associação ou referência adequadamente. Se um objeto na associação tiver sido excluído, mas não estiver marcado com **IfDeleted**, a associação não deverá ser excluída.

Essa regra de uso deve ser verificada quando o modelo de segurança CIM é definido.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Caro**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: Propriedades, referências, classes, associações, métodos

Indica se a ação implícita requer computação extensiva. O padrão é **false**.

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: associações e referências

Indica se todos os objetos em uma associação qualificada pela **exclusão** devem ser excluídos se o objeto referenciado ou a associação for excluída. O padrão é **false**.

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexa**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: Propriedades, métodos

Indica se uma propriedade de classe deve ser indexada. Quando aplicado a propriedades em classes hospedadas pelo repositório, isso só tem o significado de criar (no momento da criação da classe) uma pesquisa de consulta secundária rápida para essa propriedade.

Somente o valor **true** (padrão) é permitido.

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisível**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: associações, propriedades, métodos, referências, classes

Indica se a associação é definida somente para fins internos (por exemplo, para definição de semântica de dependência) e não deve ser exibida (por exemplo, em mapas). O padrão é **false**.

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Vários**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: Propriedades, classes

Indica se a propriedade ou classe requer uma grande quantidade de espaço de armazenamento. O padrão é **false**.

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Não \_ nulo**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: Propriedades

Indica se uma propriedade de classe não pode assumir um valor **nulo** (**VT \_ NULL**). Somente o valor **true** (padrão) é permitido.

Se esse qualificador for especificado, o WMI não permitirá a criação de instâncias com a propriedade definida como **NULL**, e as propriedades **nulas** retornarão o código de erro **\_ \_ \_ nulo E o WBEM** .

Observe que os qualificadores de [**chave**](standard-qualifiers.md) e **indexados** já implicam esse comportamento.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Operador**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: qualquer

Indicação de que o elemento de esquema é dinâmico e, portanto, preenchido por um provedor. O padrão é **NULL**. Esse qualificador é um identificador específico da implementação para a instrumentação.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: qualquer

Indica que o elemento especificado foi proposto para fazer parte de uma versão futura dos esquemas CIM, mas ainda não faz parte do esquema padrão. Em vez disso, o elemento está disponível para que os usuários testem, implementem e forneçam comentários sobre o. Com base nos comentários, o elemento pode ser adicionado ao padrão, conforme apresentado, modificado ou removido. O padrão é **false**. Uma implementação não precisa dar suporte a um elemento com este qualificador.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: Propriedades, referências, métodos, parâmetros

Tipo específico atribuído a um item de dados. O padrão é **NULL**.

Uso: você deve usar o qualificador **syntaxtype** com este qualificador.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**Sintaxetype**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: Propriedades, referências, métodos, parâmetros

Formato do qualificador de **sintaxe** . O padrão é **NULL**.

Uso: você deve usar o qualificador de **sintaxe** com este qualificador.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes, propriedades, métodos, associações, indicações, referências

Circunstâncias sob as quais um gatilho é acionado. O padrão é **NULL**. Os tipos de gatilho variam de acordo com a construção do metamodelo.

Para classes e associações, os valores válidos são:

Criar

Excluir

Atualizar

Access

Para propriedades e referências, os valores válidos são: atualização e acesso.

Para métodos, os valores válidos são antes e depois.

Para indicações, o valor legal é gerado.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Aplica-se a: Propriedades

Conjunto de valores que indica que o valor da propriedade associada é desconhecido (a propriedade não pode ser considerada como tendo um valor válido ou significativo). O padrão é **NULL**.

As convenções e restrições usadas para definir valores desconhecidos são as mesmas aplicáveis ao qualificador [**ValueMap**](standard-qualifiers.md) .

Observe que esse qualificador não pode ser substituído. Não é razoável permitir que uma subclasse trate um valor como um valor conhecido quando tratado como desconhecido por alguma classe pai.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Aplica-se a: Propriedades

Conjunto de valores que indica que o valor da propriedade associada não tem suporte (a propriedade não pode ser considerada como tendo um valor válido ou significativo). O padrão é **NULL**.

As convenções e restrições usadas para definir valores sem suporte são as mesmas aplicáveis ao qualificador [**ValueMap**](standard-qualifiers.md) .

Observe que esse qualificador não pode ser substituído. Não é razoável permitir que uma subclasse trate um valor como um valor com suporte que seja tratado como desconhecido por alguma classe pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

 




