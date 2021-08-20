---
description: Abre um armazenamento de certificados especificado.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Método Store.Open
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
ms.openlocfilehash: d70c6410d0ecb8edb91aa722bcf6f35cb9536c3ed2b7f03c2d5cb141937aeb69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897797"
---
# <a name="storeopen-method"></a>Método Store.Open

\[O **método Open** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, [**use a Classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **método Open** abre um armazenamento de [*certificados especificado.*](../secgloss/c-gly.md) Por padrão, o local DO ARMAZENAMENTO DO USUÁRIO ATUAL do CAPICOM e \_ o armazenamento MY STORE DO \_ \_ CAPICOM são abertos como somente \_ \_ leitura.

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

*StoreLocation* \[ in, opcional\]
</dt> <dd>

Um valor da [enumeração CAPICOM \_ STORE \_ LOCATION](capicom-store-location.md) que indica o local do armazenamento a ser aberto. O valor padrão é CAPICOM \_ CURRENT \_ USER \_ STORE. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**CAPICOM \_ ACTIVE \_ DIRECTORY \_ USER \_ STORE**</dt> </dl> | O armazenamento é um armazenamento do Active Directory. Nenhum erro será gerado se um armazenamento do Active Directory for aberto como leitura/gravação, mas nenhuma alteração no armazenamento será persistida. Os certificados não podem ser adicionados ou removidos dos armazenamentos do Active Directory.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**ARMAZENAMENTO DE USUÁRIO ATUAL DO CAPICOM \_ \_ \_**</dt> </dl>                             | O armazenamento é um armazenamento de usuário atual. Um armazenamento de usuário atual pode ser um armazenamento de leitura/gravação. Se for, as alterações no conteúdo do armazenamento serão persistida.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**ARMAZENAMENTO DE MÁQUINAS LOCAIS CAPICOM \_ \_ \_**</dt> </dl>                          | O armazenamento é um armazenamento de computador local. Os armazenamentos de computadores locais só poderão ser armazenamentos de leitura/gravação se o usuário tiver permissões de leitura/gravação. Se o usuário tiver permissões de leitura/gravação e se o armazenamento for aberto para leitura/gravação, as alterações no conteúdo do armazenamento serão persistida.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**ARMAZENAMENTO DE MEMÓRIA CAPICOM \_ \_**</dt> </dl>                                                | O armazenamento é um armazenamento de memória. As alterações no conteúdo do armazenamento não são persistentes.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**CAPICOM \_ SMART \_ CARD \_ USER \_ STORE**</dt> </dl>                   | A loja é o grupo de cartões inteligentes atuais. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ in, opcional\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do armazenamento de certificados do sistema a ser aberto. O valor padrão é CAPICOM \_ MY \_ STORE. Se o armazenamento for aberto de um script Web, o caractere de invertida ( ) não \\ será permitido no nome. Além dos armazenamentos definidos pelo sistema, os armazenamentos definidos pelo usuário podem ser abertos.

Esse parâmetro pode ser um armazenamento definido pelo usuário ou um dos seguintes armazenamentos de certificados do sistema.



| Valor                                                                                                                                                                            | Significado                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**CAPICOM \_ CA \_ STORE**</dt> </dl>          | Armazenamento de AC. Esse armazenamento é usado para armazenar certificados de AC intermediários.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ MY \_ STORE**</dt> </dl>          | Minha loja. Esse armazenamento é usado para certificados pessoais de um usuário.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ OTHER \_ STORE**</dt> </dl> | AddressBook Store. Esse armazenamento é usado para manter os certificados de outras pessoas.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**ARMAZENAMENTO RAIZ \_ CAPICOM \_**</dt> </dl>    | Armazenamento raiz. Esse armazenamento é usado para armazenar a AC raiz e certificados auto-assinados e confiáveis.<br/> |



 

</dd> <dt>

*OpenMode* \[ in, opcional\]
</dt> <dd>

Um valor da [enumeração CAPICOM \_ STORE OPEN \_ \_ MODE](capicom-store-open-mode.md) que indica o modo aberto do armazenamento. O valor padrão é CAPICOM \_ STORE \_ OPEN READ \_ \_ ONLY. Se o armazenamento for aberto de um script Web, esse valor será forçado para CAPICOM \_ STORE \_ OPEN \_ EXISTING \_ ONLY. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED**</dt> </dl> | Abra o armazenamento no modo de leitura/gravação se o usuário tiver permissões de leitura/gravação; caso contrário, abra o armazenamento no modo somente leitura.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ STORE SOMENTE LEITURA \_ \_ \_ ABERTA**</dt> </dl>                   | Abra o armazenamento no modo somente leitura.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**</dt> </dl>                | Abra o armazenamento no modo de leitura/gravação.<br/>                                                                                     |



 

Os sinalizadores a seguir podem ser combinados com os valores na tabela anterior usando uma operação **OR** lógica.



| Valor                                                                                                                                                                                                                              | Significado                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ STORE ABRIR SOMENTE \_ \_ EXISTENTE \_**</dt> </dl>          | Abrir somente lojas existentes; não crie um novo armazenamento. Introduzido no CAPICOM 2.0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED**</dt> </dl> | Inclua certificados arquivados ao usar o armazenamento. Introduzido no CAPICOM 2.0.<br/>   |



 

Os armazenamentos em alguns locais podem ser abertos somente no modo somente leitura. Isso inclui todas as lojas no CAPICOM LOCAL MACHINE STORE para os quais o usuário \_ não tem permissões de \_ \_ gravação. As tentativas de abrir um armazenamento como um armazenamento de leitura/gravação sem acesso e permissões adequados resultarão na falha do **método** Open. Os armazenamentos do Active Directory podem ser abertos como um armazenamento de leitura/gravação sem falha do método **Open,** mas as alterações no armazenamento não serão persistentes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se esse método for chamado em um armazenamento smartCard, interfaces de usuário do SmartCard adicionais poderão ser invocadas.

> [!IMPORTANT]
> Quando esse método é chamado de um script Web, o script precisa acessar certificados digitais no computador local. Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também terá acesso a quaisquer informações pessoais armazenadas nos certificados. Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido. Os armazenamentos abertos de um script Web forçam automaticamente o sinalizador CAPICOM \_ STORE \_ OPEN \_ EXISTING \_ ONLY.

 

Se *StoreLocation for* **CAPICOM \_ SMART CARD USER \_ \_ \_ STORE,** *StoreName* será ignorado. Nesse caso, o CAPICOM lê todos os certificados de todos os leitores disponíveis que contêm um cartão inteligente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Perto**](store-close.md)
</dt> </dl>

 

 
