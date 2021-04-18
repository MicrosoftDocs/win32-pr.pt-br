---
title: Estrutura RESOURCEHEADER
description: Contém informações sobre o cabeçalho de recurso em si e os dados específicos para esse recurso.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menus de estrutura RESOURCEHEADER e outros recursos
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812304"
---
# <a name="resourceheader-structure"></a>Estrutura RESOURCEHEADER

Contém informações sobre o cabeçalho de recurso em si e os dados específicos para esse recurso. Essa estrutura não é uma estrutura verdadeira de linguagem C, pois ela contém membros de comprimento variável. A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**DataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, dos dados que segue o cabeçalho do recurso para esse recurso específico. Ele não inclui nenhum preenchimento de arquivo entre esse recurso e qualquer recurso que o segue no arquivo de recurso.

</dd> <dt>

**Cabeçalhosize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tamanho, em bytes, dos dados de cabeçalho do recurso a seguir.

</dd> <dt>

**TYPE**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tipo de recurso. O membro de **tipo** pode ser um valor numérico ou uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do tipo. Consulte a seção de comentários a seguir para obter uma descrição dos membros do tipo **Name** ou **ordinal** .

Se o membro do **tipo** for um valor numérico, ele poderá especificar um tipo de recurso padrão ou definido pelo usuário. Se o membro for uma cadeia de caracteres, ele será um tipo de recurso definido pelo usuário. Para obter uma lista dos tipos de recursos predefinidos, consulte [tipos de recursos](/windows/desktop/menurc/resource-types).

Valores menores que 256 são reservados para uso do sistema.

</dd> <dt>

**NOME**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Um nome que identifica o recurso específico. O membro **Name** , como o membro **Type** , pode ser um valor numérico ou uma cadeia de caracteres Unicode terminada em nulo. Consulte a seção de comentários a seguir para obter uma descrição dos membros do tipo **Name** ou **ordinal** .

Você não precisa adicionar o preenchimento para o alinhamento de **DWORD** entre os membros de **tipo** e **nome** porque eles contêm dados do **Word** . No entanto, talvez seja necessário adicionar uma **palavra** de preenchimento após o membro **nome** para alinhar o restante do cabeçalho nos limites **DWORD** .

</dd> <dt>

**Versão de**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Uma versão de dados de recurso predefinida. Isso determinará qual versão dos dados de recursos o aplicativo deve usar.

</dd> <dt>

**MemoryFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Um conjunto de sinalizadores de atributo que pode descrever o estado do recurso. Modificadores no. Arquivo de script RC atribua esses atributos ao recurso. Os identificadores de script podem atribuir os seguintes valores de sinalizador.

Os aplicativos não usam nenhum desses atributos. Os atributos são permitidos no script para compatibilidade com versões anteriores com scripts existentes, mas são ignorados. Os recursos são carregados quando o módulo correspondente é carregado e liberados quando o módulo é descarregado.

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**Móvel** (0x0010)


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

**corrigido** (~ móvel)


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**Puro** (0x0020)


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**impuro** (~ puro)


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**Pré-carregar** (0x0040)


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL** (~ pré-carregar)


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

**Descartado** (0x1000)


</dt> <dd></dd> </dl> </dd> <dt>

**LanguageId**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O idioma do recurso ou conjunto de recursos. Defina o valor para esse membro com a instrução de definição de recurso de [linguagem](./language-statement.md) opcional. Os parâmetros são constantes do arquivo Winnt. h.

Cada recurso inclui um identificador de idioma para que o sistema ou aplicativo possa selecionar um idioma apropriado para a localidade atual do sistema. Se houver vários recursos do mesmo tipo e nome que diferem apenas no idioma das cadeias de caracteres dentro dos recursos, você precisará especificar um **LanguageID** para cada um.

</dd> <dt>

**Versão**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Um número de versão definido pelo usuário para os dados de recurso que as ferramentas podem usar para ler e gravar arquivos de recursos. Defina esse valor com a instrução de definição de recurso de [versão](./version-statement.md) opcional.

</dd> <dt>

**Características**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica informações definidas pelo usuário sobre o recurso que as ferramentas podem usar para ler e gravar arquivos de recursos. Defina esse valor com a instrução de definição de recurso [características](./characteristics-statement.md) opcionais.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um membro de tipo de variável é chamado de **nome** ou membro **ordinal** e é usado na maioria dos lugares no arquivo de recurso onde um identificador é exibido. A primeira **palavra** de um **nome** ou membro de tipo **ordinal** indica se o membro é um valor numérico ou uma cadeia de caracteres. Se a primeira **palavra** no membro for igual ao valor 0xFFFF, que é um caractere Unicode inválido, a **palavra** a seguir será um número de tipo. Caso contrário, o membro contém uma cadeia de caracteres Unicode e a primeira **palavra** no membro é o primeiro caractere na cadeia de caracteres de nome. Para obter informações adicionais sobre instruções de definição de recurso, consulte [instruções de definição de recurso](./resource-definition-statements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Conceitua**
</dt> <dt>

[Recursos](resources.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Instrução de características](./characteristics-statement.md)
</dt> <dt>

[Instrução de linguagem](./language-statement.md)
</dt> <dt>

[Instrução de versão](./version-statement.md)
</dt> </dl>

 

