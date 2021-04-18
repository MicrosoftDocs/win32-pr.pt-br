---
description: Abre um objeto de diretório existente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Função NtOpenDirectoryObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751953"
---
# <a name="ntopendirectoryobject-function"></a>Função NtOpenDirectoryObject

\[Essa função pode ser alterada ou não estar disponível no futuro.\]

Abre um objeto de diretório existente.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DirectoryHandle* \[ fora\]
</dt> <dd>

Um identificador para o objeto de diretório aberto recentemente.

</dd> <dt>

*DesiredAccess* \[ no\]
</dt> <dd>

Uma [**\_ máscara de acesso**](../secauthz/access-mask.md) que especifica o acesso solicitado ao objeto de diretório. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                      | Significado                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**Do diretório \_**</dt> <dt>0X0001</dt> de consulta </dl>                                            | Acesso de consulta ao objeto de diretório.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**Do diretório \_ PERCORRER**</dt> <dt>0x0002</dt> </dl>                                   | Acesso de pesquisa de nome ao objeto de diretório.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**Do diretório \_ CRIAR \_**</dt> <dt>0x0004</dt> de objeto </dl>                   | Acesso de criação de nome ao objeto de diretório.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**Do diretório \_ CRIAR \_ subdiretório**</dt> <dt>0x0008</dt> </dl> | Acesso de criação de subdiretório ao objeto de diretório.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**Do diretório \_ Todos \_ os**</dt> <dt>direitos padrão de acesso \_ \_ necessários \| 0xF</dt> </dl> | Todos os direitos anteriores, além **dos \_ direitos padrão \_ necessários**.<br/> |



 

</dd> <dt>

*Objetoattributes* \[ no\]
</dt> <dd>

Os atributos para o objeto de diretório. Para inicializar a estrutura de **\_ atributos de objeto** , use a macro **InitializeObjectAttributes** . Para obter mais informações, consulte a documentação para esses itens na documentação do WDK.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o STATUS \_ êxito ou um status de erro. Os códigos de status possíveis incluem o seguinte.



| Código de retorno                                                                                                       | Descrição                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATUS de \_ recursos insuficientes \_**</dt> </dl>    | Não foi possível alocar um buffer temporário exigido por essa função.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**parâmetro de STATUS \_ inválido \_**</dt> </dl>         | O parâmetro objectAttributes especificado era um ponteiro **nulo** , não um ponteiro válido para uma estrutura de **\_ atributos de objeto** ou alguns dos membros especificados na estrutura de **\_ atributos de objeto** não eram válidos.<br/>                                                                          |
| <dl> <dt>**nome do objeto de STATUS \_ \_ \_ inválido**</dt> </dl>      | O parâmetro *objectAttributes* continha um membro **objectname** na estrutura de **\_ atributos de objeto** que não era válida porque uma cadeia de caracteres vazia foi encontrada após o caractere **\_ \_ \_ separador de caminho de nome de objeto** .<br/>                                                                        |
| <dl> <dt>**nome do objeto de STATUS \_ \_ \_ não \_ encontrado**</dt> </dl>   | O parâmetro *objectAttributes* continha um membro **objectname** na estrutura de **\_ atributos de objeto** que não pôde ser encontrada.<br/>                                                                                                                                                           |
| <dl> <dt>**caminho do objeto de STATUS \_ \_ \_ não \_ encontrado**</dt> </dl>   | O parâmetro *objectAttributes* continha um membro **objectname** na estrutura de **\_ atributos de objeto** com um caminho de objeto que não pôde ser encontrado. <br/>                                                                                                                                      |
| <dl> <dt>**Status \_ do sintaxe de caminho de objeto \_ \_ \_ inadequada**</dt> </dl> | O parâmetro *objectAttributes* não continha um membro **RootDirectory** , mas o membro **objectname** na estrutura de **\_ atributos de objeto** era uma cadeia de caracteres vazia ou não continha um caractere **\_ \_ \_ separador de caminho de nome de objeto** . Isso indica uma sintaxe incorreta para o caminho do objeto.<br/> |



 

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
