---
title: Sintaxe de atributo ADSI
description: Cada atributo no diretório tem uma sintaxe associada. Por exemplo, inteiro, Cadeia de caracteres, numérico e assim por diante. A ADSI define sua própria sintaxe que é mapeada para a sintaxe do diretório nativo. Esta seção descreve os tipos de sintaxes de atributo no ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- atributos ADSI, sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641828"
---
# <a name="adsi-attribute-syntax"></a>Sintaxe de atributo ADSI

Cada atributo no diretório tem uma sintaxe associada. Por exemplo, inteiro, Cadeia de caracteres, numérico e assim por diante. A ADSI define sua própria sintaxe que é mapeada para a sintaxe do diretório nativo. Esta seção descreve os tipos de sintaxes de atributo no ADSI.

## <a name="distinguished-name-string"></a>Cadeia de caracteres de nome distinto


```VB
Syntax Type: ADSTYPE_DN_STRING
```



O nome distinto é útil para vincular dois objetos juntos. Por exemplo, ele pode criar um link que torna o objeto Alice um gerente do objeto Bob. Se o objeto Alice se mover para um local diferente, o link do gerente entre Alice e Bob será atualizado automaticamente.

O nome distinto deve conter um objeto de nome distinto válido. Se o nome diferenciado não corresponder a um objeto existente válido, a maioria dos servidores rejeitará a solicitação e retornará um erro de violação de restrição.

Exemplos:


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Cadeia de caracteres Exact maiúsculas e maiúsculas e minúsculas


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



A cadeia exata de maiúsculas e minúsculas é uma cadeia de caracteres que diferencia maiúsculas de minúsculas quando a cadeia de caracteres ignora maiúsculas e minúsculas Uma grande porcentagem de atributos no diretório usa essa sintaxe.

> [!Note]  
> O diretório pode ou não armazenar isso como uma cadeia de caracteres Unicode. No entanto, a ADSI aceita e retorna cadeias de caracteres Unicode.

 

Exemplo:


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a>Cadeia de caracteres imprimível


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



Essa sintaxe é usada para atributos com valores de cadeia de caracteres em que letras maiúsculas e minúsculas são consideradas desiguais para comparações, por exemplo, "FABRIKAM" e "fabrikam" não correspondem. A ADSI aceita qualquer conteúdo para uma cadeia de caracteres imprimível; Ele não tenta verificar se eles estão realmente imprimíveis.

## <a name="numeric-string"></a>Cadeia de caracteres numérica


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



Nessa sintaxe, cadeias de caracteres correspondem como em cadeias imprimíveis, exceto que todos os caracteres de espaço são ignorados em comparações. A ADSI não executa a verificação de valor para garantir que somente numerais e espaços apareçam em valores dessa sintaxe. Active Directory aceita qualquer conteúdo para uma cadeia de caracteres numérica; Ele não verifica se os caracteres são numéricos.

## <a name="utc-time"></a>Hora UTC


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Essa sintaxe armazena a data e a hora em uma única cadeia de caracteres. O formato da cadeia de caracteres consiste em três partes concatenadas: (1) YYMMDD; (2) HHMM ou HHMMSS (ambos são aceitáveis); e (3) "Z" para indicar que o tempo fornecido é Greenwich Mean Time (GMT) ou "+/-HHMM" para indicar que a hora fornecida é a hora local com o diferencial fornecido do GMT. O diferencial é baseado na fórmula: GMT = local + diferencial.

> [!Note]  
> Os dois primeiros dígitos do ano não são armazenados nessa cadeia de caracteres.

 

Alguns exemplos de valores válidos são "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503 + 0130". Essa cadeia de caracteres é armazenada como caracteres ASCII de byte único e nenhum número de página de código é armazenado com ele.

Embora a ordenação tenha suporte, ela é feita apenas como uma classificação de cadeia de caracteres que não diferencia maiúsculas de minúsculas, Não interpretando adequadamente o significado das cadeias.

Qualquer valor de cadeia de caracteres válido é aceito. Nenhuma tentativa é feita para garantir que a cadeia de caracteres contenha uma cadeia de caracteres de tempo válida.

## <a name="generalized-time"></a>Tempo generalizado


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Se um novo atributo para armazenar valores de tempo estiver sendo definido, a sintaxe GeneralizedTime deverá ser usada. A sintaxe GeneralizedTime usa quatro caracteres para representar o ano em vez de dois como com UTCTime.

O formato da sintaxe GeneralizedTime é "AAAAMMDDHHMMSS. 0Z". Um exemplo de um valor aceitável é "20010928060000.0 Z". O "Z" indica que não há diferencial de tempo. Active Directory armazena data/hora como GMT (hora de Greenwich). Se nenhum diferencial de tempo for especificado, GMT será o padrão.

Se o tempo for especificado em um fuso horário diferente de GMT, o diferencial entre o fuso horário e o GMT será acrescentado à cadeia de caracteres em vez de "Z" no formato "AAAAMMDDHHMMSS. 0 \[ +/- \] hhmm". Um exemplo de um valor aceitável é "20010928060000.0 + 0200".

O diferencial é baseado na fórmula: GMT = local + diferencial.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory aceita apenas um valor de 32 bits assinado para essa sintaxe. Ele manipula zero como **falso** e todos os valores diferentes de zero como **verdadeiro**.

## <a name="integer"></a>Inteiro


```VB
Syntax Type: ADSTYPE_INTEGER
```



Um valor numérico assinado de 32 bits.

## <a name="large-integer"></a>Inteiro grande


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Um valor numérico assinado de 64 bits. Inteiros grandes são realmente implementados como objetos COM na interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) . Os métodos **HighPart** e **LowPart** são usados para acessar as metades de 2 32 bits do valor inteiro grande.

Exemplo:


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Cadeia de caracteres de octeto


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Uma cadeia de caracteres de octeto é retornada como uma matriz variante de bytes. Isso consiste em uma contagem de tamanho (número de octetos) seguida por uma série de octetos. Um octeto é um byte de 8 bits, portanto, uma série de octetos é uma cadeia de caracteres de dados binários.

## <a name="object-class"></a>Classe de objeto


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



A classe de objeto é um identificador de objeto exclusivo para uma determinada classe de esquema. A classe de cada instância de objeto é identificada pelo atributo **objectClass** . Quando criado, você nunca pode alterar uma classe de objeto. **objectClass** é um atributo com vários valores. Ele lista a classe específica do objeto e as classes de todas as classes estruturais ou abstratas das quais a classe específica foi derivada. Isso inclui top, a classe da qual todas as outras classes são derivadas basicamente. Active Directory não listar as classes auxiliares no atributo **objectClass** .

## <a name="security-descriptor"></a>Descritor de Segurança


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



Os direitos de acesso definem quais capacidades uma entidade de segurança tem ao tentar executar uma operação em um objeto Active Directory. Um descritor de segurança descreve as informações de controle de acesso associadas a um objeto.

O descritor de segurança é armazenado como uma propriedade de um objeto de diretório na propriedade **nTSecurityDescriptor** . Quando um usuário autenticado tenta acessar um objeto de diretório, o servidor de diretório determina o acesso concedido ou negado ao usuário com base no descritor de segurança do objeto.

A enumeração de [**\_ \_ \_ enumeração de controle SD do ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) especifica sinalizadores de controle para um descritor de segurança.

O exemplo de código a seguir mostra como obter um descritor de segurança.


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxes para atributos de Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[Escolhendo uma sintaxe](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[Como especificar valores de comparação](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 