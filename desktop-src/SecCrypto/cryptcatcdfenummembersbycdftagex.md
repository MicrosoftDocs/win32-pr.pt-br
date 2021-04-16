---
description: Enumera os membros do arquivo individual na seção CatalogFiles de um arquivo de definição de catálogo (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Função CryptCATCDFEnumMembersByCDFTagEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501549"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>Função CryptCATCDFEnumMembersByCDFTagEx

\[A função **CryptCATCDFEnumMembersByCDFTagEx** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A função **CryptCATCDFEnumMembersByCDFTagEx** enumera os membros de arquivo individuais na seção **CatalogFiles** de um arquivo de definição de catálogo (CDF). **CryptCATCDFEnumMembersByCDFTagEx** é chamado por [MakeCat](makecat.md).

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCDF* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszPrevCDFTag* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em **nulo** que identifica o membro do arquivo de catálogo.

</dd> <dt>

*pfnParseError* \[ no\]
</dt> <dd>

Um ponteiro para uma função definida pelo usuário para manipular erros de análise de arquivo.

</dd> <dt>

*ppMember* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contém as informações de membro do arquivo.

</dd> <dt>

*fContinueOnError* \[ no\]
</dt> <dd>

Um valor que especifica se a memória deve ser mantida em uma referência ao último membro enumerado.

</dd> <dt>

*pvReserved* \[ no\]
</dt> <dd>

Este parâmetro é reservado; Não o use.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Após o êxito, essa função retorna um ponteiro para uma cadeia de caracteres terminada em **nulo** que identifica um membro de arquivo na seção **CATALOGFILES** de um CDF. A função **CryptCATCDFEnumMembersByCDFTagEx** retornará um ponteiro **nulo** se falhar.

## <a name="remarks"></a>Comentários

Normalmente, você chama essa função em um loop para enumerar todos os membros do arquivo de catálogo em um CDF. Antes de entrar no loop, defina *pwszPrevCDFTag* como **nulo**. A função retorna um ponteiro para o primeiro membro. Defina *pwszPrevCDFTag* como o valor de retorno da função para iterações subsequentes do loop.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a sequência correta de atribuições para o parâmetro *pwszPrevCDFTag* ( `pwszMemberTag` ).


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MakeCat](makecat.md)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
