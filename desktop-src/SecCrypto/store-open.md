---
description: Abre um repositório de certificados especificado.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Método Store. Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783226"
---
# <a name="storeopen-method"></a>Método Store. Open

\[O método **Open** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Open** abre um [*repositório de certificados*](../secgloss/c-gly.md)especificado. Por padrão, o local de repositório do usuário atual do CAPICOM \_ \_ e o CAPICOM do repositório de \_ \_ \_ armazenamento são abertos como somente leitura.

## <a name="syntax"></a>Sintaxe


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StoreLocation* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [do \_ \_ local de armazenamento capicor](capicom-store-location.md) que indica o local do repositório a ser aberto. O valor padrão é capicote \_ \_ user \_ Store atual. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**armazenamento de usuários do CAPICOM \_ \_ do Active Directory \_ \_**</dt> </dl> | O repositório é um repositório Active Directory. Nenhum erro será gerado se um repositório de Active Directory for aberto como leitura/gravação, mas quaisquer alterações no repositório não serão persistidas. Os certificados não podem ser adicionados ou removidos de repositórios Active Directory.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_armazenamento de \_ usuário \_ atual do CAPICOM**</dt> </dl>                             | O repositório é um armazenamento de usuário atual. Um armazenamento de usuário atual pode ser um repositório de leitura/gravação. Se for, as alterações no conteúdo do repositório serão persistidas.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**CAPICOM do \_ \_ armazenamento do computador local \_**</dt> </dl>                          | O repositório é um repositório do computador local. As lojas de computadores locais poderão ser armazenamentos de leitura/gravação somente se o usuário tiver permissões de leitura/gravação. Se o usuário tiver permissões de leitura/gravação e se o repositório for aberto como leitura/gravação, as alterações no conteúdo do repositório serão persistidas.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_armazenamento de memória CApicom \_**</dt> </dl>                                                | O repositório é um repositório de memória. As alterações no conteúdo da loja não são persistentes.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_armazenamento de \_ usuário do cartão inteligente \_ CAPICOM \_**</dt> </dl>                   | O repositório é o grupo de cartões inteligentes presentes. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ em, opcional\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do repositório de certificados do sistema a ser aberto. O valor padrão é capicore \_ My \_ Store. Se o repositório for aberto de um script da Web, o caractere de barra invertida ( \\ ) não será permitido no nome. Além dos armazenamentos definidos pelo sistema, os armazenamentos definidos pelo usuário podem ser abertos.

Esse parâmetro pode ser um repositório definido pelo usuário ou um dos seguintes repositórios de certificados do sistema.



| Valor                                                                                                                                                                            | Significado                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**\_armazenamento de AC CApicom \_**</dt> </dl>          | Repositório de AC. Esse armazenamento é usado para armazenar certificados de AC intermediários.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ meu \_ repositório**</dt> </dl>          | Meu repositório. Esse armazenamento é usado para certificados pessoais de um usuário.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ outro \_ armazenamento**</dt> </dl> | Catálogo Store. Esse armazenamento é usado para manter os certificados de outros.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**CAPICOM de \_ \_ armazenamento raiz**</dt> </dl>    | Armazenamento raiz. Esse armazenamento é usado para armazenar a autoridade de certificação raiz e certificados confiáveis e auto-assinados.<br/> |



 

</dd> <dt>

*OpenMode* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [do \_ \_ \_ modo de abertura do armazenamento capicor](capicom-store-open-mode.md) que indica o modo aberto da loja. O valor padrão é capicote \_ Store \_ Open \_ Read \_ only. Se o repositório for aberto de um script da Web, esse valor será forçado ao armazenamento CAPICOM \_ \_ abrir \_ \_ somente existente. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**\_ \_ \_ máximo permitido de armazenamento \_ de CAPICOM**</dt> </dl> | Abra o repositório no modo de leitura/gravação se o usuário tiver permissões de leitura/gravação; caso contrário, abra o repositório no modo somente leitura.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM de \_ leitura do armazenamento \_ \_ \_**</dt> </dl>                   | Abra o repositório no modo somente leitura.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**o CAPICOM de \_ \_ leitura e \_ \_ gravação aberta**</dt> </dl>                | Abra o repositório no modo de leitura/gravação.<br/>                                                                                     |



 

Os sinalizadores a seguir podem ser combinados com os valores na tabela anterior usando uma operação **or** lógica.



| Valor                                                                                                                                                                                                                              | Significado                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ Store \_ abrir \_ \_ somente existente**</dt> </dl>          | Abrir somente repositórios existentes; Não crie um novo repositório. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**o CAPICOM de \_ Store \_ aberto \_ incluem \_ arquivados**</dt> </dl> | Inclua certificados arquivados ao usar o repositório. Introduzido no CAPICOM 2,0.<br/>   |



 

Os repositórios em alguns locais podem ser abertos somente no modo somente leitura. Isso inclui todas as lojas no \_ repositório do computador local CApicom \_ \_ para o qual o usuário não tem permissões de gravação. Tenta abrir um repositório como um repositório de leitura/gravação sem acesso adequado e as permissões resultarão na falha do método **Open** . Active Directory armazenamentos podem ser abertos como um repositório de leitura/gravação sem falha do método **Open** , mas as alterações no repositório não serão persistidas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se esse método for chamado em um repositório de cartão inteligente, outras interfaces de usuário de cartão inteligente poderão ser invocadas.

> [!IMPORTANT]
> Quando esse método é chamado de um script da Web, o script precisa acessar certificados digitais no computador local. Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também obterá acesso a todas as informações pessoais armazenadas nos certificados. Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido. Lojas abertas de um script da Web automaticamente forçam o sinalizador CAPICOM \_ \_ Open \_ existing Store \_ .

 

Se *StoreLocation* for **o \_ \_ armazenamento de \_ usuário \_ do cartão inteligente CAPICOM**, *StoreName* será ignorado. Nesse caso, o CAPICOM lê todos os certificados de todos os leitores disponíveis que contêm um cartão inteligente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Fechar**](store-close.md)
</dt> </dl>

 

 
