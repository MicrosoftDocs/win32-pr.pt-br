---
description: Explica as cadeias de caracteres usadas em uma entrada de controle de acesso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Cadeias de Caracteres ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60e8f4f5d3cd94f6e871b3b4962d2d548afa003c3bd4aa37a1ae8f008ce1a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785397"
---
# <a name="ace-strings"></a>Cadeias de Caracteres ACE

A [linguagem de definição do descritor de segurança](security-descriptor-definition-language.md) (SDDL) usa cadeias de caracteres Ace nos componentes DACL e SACL de uma cadeia de caracteres de [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) .

Conforme mostrado nos exemplos de [formato de cadeia de caracteres do descritor de segurança](security-descriptor-string-format.md) , cada ACE em uma cadeia de caracteres de descritor de segurança é colocado entre parênteses. Os campos da ACE estão na seguinte ordem e são separados por ponto e vírgula (;).

> [!Note]  
> Há um formato diferente para as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) condicionais que outros tipos de Ace. Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Campos

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**tipo de Ace \_**
</dt> <dd>

Uma cadeia de caracteres que indica o valor do membro **AceType** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . A cadeia do tipo ACE pode ser uma das seguintes cadeias de caracteres definidas em SDDL. h.



| ACE tipo String | Constante em SDDL. h                      | Valor de AceType                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "A"             | acesso de SDDL \_ \_ permitido                   | \_tipo de \_ Ace \_ permitido de acesso                                                                                                                                         |
| "D"             | acesso de SDDL \_ \_ negado                    | tipo de ACE de acesso \_ negado \_ \_                                                                                                                                          |
| OA            | \_acesso de objeto SDDL \_ \_ permitido           | \_tipo de \_ ACE de objeto permitido \_ de acesso \_                                                                                                                                 |
| OD            | \_ \_ acesso \_ negado ao objeto SDDL            | tipo de ACE de objeto de acesso \_ negado \_ \_ \_                                                                                                                                  |
| AU            | auditoria de SDDL \_                             | \_tipo de \_ ACE de auditoria do sistema \_                                                                                                                                           |
| "AL"            | \_alarme SDDL                             | \_tipo de \_ Ace do alarme do sistema \_                                                                                                                                           |
| CN            | \_auditoria de objeto SDDL \_                     | \_ \_ tipo ACE do objeto Audit \_ do \_ sistema                                                                                                                                   |
| OL            | \_alarme do objeto SDDL \_                     | \_ \_ tipo ACE do objeto Alarm \_ do \_ sistema                                                                                                                                   |
| "ML"            | \_rótulo obrigatório de SDDL \_                  | \_tipo de \_ ACE de rótulo obrigatório do sistema \_ \_ **Windows Server 2003:** não disponível.                                                                                        |
| XA            | \_acesso de retorno de chamada SDDL \_ \_ permitido         | acesso \_ permitido ao \_ tipo de chamada \_ ACE \_ **Windows server 2008, Windows Vista e Windows server 2003:** não disponível.                                                |
| XD            | \_acesso de retorno de chamada SDDL \_ \_ negado          | acesso \_ negado \_ chamada \_ \_ tipo ACE **Windows server 2008, Windows Vista e Windows server 2003:** não disponível.                                                 |
| ARQUITETURA            | \_atributo de recurso SDDL \_               | \_tipo de atributo de recurso do sistema \_ \_ \_ **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** não disponível.<br/> |
| SP3            | ID da política com \_ escopo SDDL \_ \_                | \_ID da política com escopo do sistema \_ \_ \_ ACE \_ tipo **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows Server 2003:** não disponível.<br/>  |
| "XU"            | \_auditoria de retorno de chamada SDDL \_                   | \_tipo de \_ retorno de chamada \_ de auditoria do sistema \_ **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows Server 2003:** não disponível.<br/>     |
| ZA            | \_acesso de objeto de retorno de chamada SDDL \_ \_ \_ permitido | acesso \_ permitido \_ retorno de chamada \_ ACE \_ tipo **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** não disponível.<br/>   |
| TL            | \_rótulo de \_ confiança do processo SDDL \_             | \_ \_ rótulo de confiança do processo do sistema \_ \_ \_ tipo ACE **Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows Server 2003:** não disponível. |
| Flórida            | \_filtro de acesso SDDL \_                    | \_ \_ \_ tipo de ACE de filtro de acesso do sistema \_ **Windows Server 2016, Windows 10 versão 1607, Windows 10 versão 1511, Windows 10 versão 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** não disponível. |
 

> [!Note]  
> Se **o \_ tipo ACE** for \_ \_ \_ o tipo de ACE de objeto permitido \_ de acesso e nenhum GUID de **objeto \_** nem **herdar o \_ \_ GUID de objeto** tiver um [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) especificado, [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converterá o **\_ tipo ACE** para acessar o \_ \_ tipo de Ace permitido \_ .

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**sinalizadores de Ace \_**
</dt> <dd>

Uma cadeia de caracteres que indica o valor do membro **AceFlags** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . A cadeia de caracteres de sinalizadores de ACE pode ser uma concatenação das seguintes seqüências definidas em SDDL. h.



| Cadeia de caracteres de sinalizadores ACE | Constante em SDDL. h       | Valor de AceFlag                 |
|------------------|--------------------------|-------------------------------|
| CIS             | \_herança de contêiner SDDL \_ | \_Ace herdar contêiner \_       |
| Oi             | \_herança de objeto SDDL \_    | \_ACE de herança de objeto \_          |
| NP             | SDDL \_ sem \_ propagação      | NENHUMA \_ ACE de \_ herança de propagação \_   |
| I             | herança de SDDL \_ \_ somente      | HERDAr \_ somente \_ Ace            |
| “ID”             | SDDL \_ herdada          | Ace HERDAdo \_                |
| ADMINISTRADOR             | \_êxito na auditoria de SDDL \_     | \_sinalizador de \_ ACE de acesso bem-sucedido \_ |
| ATIVO             | \_falha de auditoria de SDDL \_     | \_sinalizador de \_ ACE de acesso com falha \_     |
| TP             | \_filtro de confiança \_ protegida \_ SDDL | \_ \_ \_ \_ sinalizador de ACE de filtro protegido **de confiança Windows Server 2016, Windows 10 versão 1607, Windows 10 versão 1511, Windows 10 versão 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** não disponível. |
| CD             | SDDL \_ crítico           | \_sinalizador de ACE crítico \_ **Windows server versão 1803, Windows 10 versão 1803, Windows Server versão 1709, Windows 10 versão 1709, Windows 10 versão 1703, Windows Server 2016, Windows 10 versão 1607, Windows 10 versão 1511, Windows 10 versão 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows Server 2003:** não disponível. |
 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**privilégios**
</dt> <dd>

Uma cadeia de caracteres que indica os [direitos de acesso](access-rights-and-access-masks.md) controlados pela Ace. Essa cadeia de caracteres pode ser uma representação de cadeia de caracteres hexadecimal dos direitos de acesso, como "0x7800003F", ou pode ser uma concatenação das cadeias de caracteres a seguir.



### <a name="generic-access-rights"></a>Direitos de acesso genéricos

| Cadeia de direitos de acesso | Constante em SDDL. h | Valor direito de acesso |
|----------------------|--------------------|--------------------|
| 3º                 | \_ \_ todos os genéricos SDDL | \_tudo genérico       |
| GR                 | \_leitura genérica de SDDL \_ | \_leitura genérica     |
| GW                 | \_gravação genérica \_ SDDL | \_gravação genérica |
| GX                 | \_execução genérica de SDDL \_ | \_execução genérica |


### <a name="standard-access-rights"></a>Direitos de acesso padrão

| Cadeia de direitos de acesso | Constante em SDDL. h | Valor direito de acesso |
|----------------------|--------------------|--------------------|
| RC                 | \_controle de leitura de SDDL \_ | controle de leitura \_      |
| SD                 | \_exclusão padrão de SDDL \_ | DELETE          |
| WD                 | \_DAC de gravação de SDDL \_ | GRAVAR \_ DAC            |
| OIS                 | \_proprietário da gravação SDDL \_ | proprietário da gravação \_        |

### <a name="directory-service-object-access-rights"></a>Direitos de acesso a objeto de serviço de diretório

| Cadeia de direitos de acesso | Constante em SDDL. h | Valor direito de acesso |
|----------------------|--------------------|--------------------|
| RP                 | \_propriedade de leitura de SDDL \_ | ADS \_ direito \_ de \_ leitura de DS \_ de AD |
| PROCESSADOR                 | \_propriedade de gravação SDDL \_ | publicidade \_ de \_ gravação DS do \_ ad \_ |
| CC                 | \_criar \_ filho de SDDL | \_direito de \_ criação de DS do AD do ADS \_ \_ |
| ORIGEM                 | \_excluir \_ filho de SDDL | \_direito de \_ exclusão de DS do AD do ADS \_ \_ |
| LCs                 | \_lista de \_ filhos de SDDL | lista de anúncios \_ à direita \_ ACTRL \_ DS \_ |
| CM                 | \_auto- \_ gravação de SDDL    | ANÚNCIOS \_ do lado direito do \_ ad \_ |
| LO                  | \_objeto da lista SDDL \_ | \_objeto de \_ lista de DS direito do ADS \_ \_ |
| DT                 | \_árvore de exclusão de SDDL \_ | \_árvore de \_ exclusão de DS do lado do ADS \_ \_ |
| CD                  | \_acesso de controle SDDL \_ | \_acesso ao \_ controle de DS direito do ADS \_ \_ |

### <a name="file-access-rights"></a>Direitos de acesso a arquivos

| Cadeia de direitos de acesso | Constante em SDDL. h | Valor direito de acesso |
|----------------------|--------------------|--------------------|
| ATIVO                 | \_arquivo SDDL \_ All    | ARQUIVAr \_ todo o \_ acesso   |
| FR                 | \_leitura de arquivo SDDL \_   | \_leitura genérica do arquivo \_ |
| FW                 | \_gravação de arquivo SDDL \_  | \_gravação genérica de arquivo \_ |
| EFEITO                 | \_execução de arquivo SDDL \_ | \_execução genérica do arquivo \_ |


### <a name="registry-key-access-rights"></a>Direitos de acesso à chave do registro

| Cadeia de direitos de acesso | Constante em SDDL. h | Valor direito de acesso |
|----------------------|--------------------|--------------------|
| Ka                 | \_chave SDDL \_ All     | CHAVE de \_ todo o \_ acesso   |
| Coreia                 | \_leitura de chave SDDL \_    | leitura de chave \_          |
| KW                 | \_gravação de chave SDDL \_   | gravação de chave \_         |
| "KX"                 | \_execução da chave SDDL \_ | \_executar chave       |

### <a name="mandatory-label-rights"></a>Direitos de rótulo obrigatórios

| Cadeia de direitos de acesso | Constante em SDDL. h | Valor direito de acesso |
|----------------------|--------------------|--------------------|
| NR                 | SDDL \_ não \_ lido \_ | \_rótulo obrigatório \_ do \_ sistema \_ não \_ ler **Windows server 2008, Windows Vista e Windows server 2003:** não disponível. |
| NW                 | SDDL \_ sem \_ gravação \_ | \_rótulo obrigatório \_ do \_ sistema \_ sem \_ gravação **Windows server 2008, Windows Vista e Windows server 2003:** não disponível. |
| NX                 | SDDL \_ não \_ executar \_ | \_rótulo obrigatório \_ do \_ sistema \_ não \_ executar **Windows server 2008, Windows Vista e Windows Server 2003:** não disponível. |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID do objeto \_**
</dt> <dd>

Uma representação de cadeia de caracteres de um GUID que indica o valor do membro **objecttype** de uma estrutura ACE específica de objeto, [**como \_ \_ \_ ACE de objeto permitido de acesso**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). A cadeia de caracteres GUID usa o formato retornado pela função [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

A tabela a seguir lista alguns GUIDs de objeto usados com frequência.



| Direitos e GUID                         | Permissão      |
|-----------------------------------------|-----------------|
| CR; ab721a53-1e2f-11D0-9819-00aa0040529b | Alterar senha |
| CR; 00299570-246d-11D0-A768-00aa006e0529 | Redefinir senha  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**herdar \_ GUID do objeto \_**
</dt> <dd>

Uma representação de cadeia de caracteres de um GUID que indica o valor do membro **InheritedObjectType** de uma estrutura ACE específica de objeto. A cadeia de caracteres GUID usa o formato [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**Sid da conta \_**
</dt> <dd>

[Cadeia de caracteres de Sid](sid-strings.md) que identifica o [confiável](trustees.md) da Ace.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**atributo de recurso \_**
</dt> <dd>

\[OPCIONAL \] o atributo de recurso \_ é apenas para ACEs de recurso e é opcional. Uma cadeia de caracteres que indica o tipo de dados. O tipo de dados Ace do atributo de recurso pode ser um dos seguintes tipos de dados definidos em SDDL. h.

O \# sinal "" é sinônimo de "0" em atributos de recurso. Por exemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) é equivalente a e interpretado como D:ai (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** Os atributos de recurso não estão disponíveis.



| Cadeia de caracteres de tipo de dados ACE de atributo de recurso | Constante em SDDL. h | Tipo de dados        |
|-----------------------------------------|--------------------|------------------|
| It                                    | SDDL \_ int          | Inteiro assinado   |
| Tu                                    | SDDL \_ uint         | Inteiro não assinado |
| CALs                                    | \_WSTRING SDDL      | Cadeia de caracteres larga      |
| TD                                    | \_SID SDDL          | SID              |
| TX                                    | BLOB de SDDL \_         | Cadeia de caracteres de octeto     |
| TB                                    | \_booliano SDDL      | Boolean          |



 

</dd> </dl>

O exemplo a seguir mostra uma cadeia de caracteres ACE para uma ACE permitida pelo Access. Ele não é uma ACE específica do objeto, portanto, não tem informações nos campos **\_ GUID do objeto** e **herdar \_ \_ GUID do objeto** . O campo de **\_ sinalizadores de Ace** também está vazio, o que indica que nenhum dos sinalizadores de Ace está definido.


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



A cadeia de caracteres ACE mostrada acima descreve as informações de ACE a seguir.


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



o exemplo a seguir mostra um arquivo classificado com declarações de recurso para Windows e linguagem SQL (SQL) com pfs definido como alto impacto comercial.


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



A cadeia de caracteres ACE mostrada acima descreve as informações de ACE a seguir.


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



Para obter mais informações, consulte [Security Descriptor String Format](security-descriptor-string-format.md) e [Sid Strings](sid-strings.md). Para ACEs condicionais, consulte [linguagem de definição do descritor de segurança para aces condicionais](security-descriptor-definition-language-for-conditional-aces-.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\[MS-DTYP \] : linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

