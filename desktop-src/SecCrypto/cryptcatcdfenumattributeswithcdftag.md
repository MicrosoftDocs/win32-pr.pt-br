---
description: Enumera os atributos dos arquivos de membro na seção CatalogFiles de um arquivo de definição de catálogo (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Função CryptCATCDFEnumAttributesWithCDFTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501548"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>Função CryptCATCDFEnumAttributesWithCDFTag

\[A função **CryptCATCDFEnumAttributesWithCDFTag** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A função **CryptCATCDFEnumAttributesWithCDFTag** enumera os atributos dos arquivos de membro na seção **CatalogFiles** de um arquivo de definição de catálogo (CDF). **CryptCATCDFEnumAttributesWithCDFTag** é chamado por [MakeCat](makecat.md).

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCDF* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*pwszMemberTag* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em **nulo** que identifica o membro do arquivo de catálogo.

</dd> <dt>

*pMember* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) que contém as informações do membro.

</dd> <dt>

*pPrevAttr* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) para um atributo de membro de arquivo no CDF apontado por *pCDF*.

</dd> <dt>

*pfnParseError* \[ no\]
</dt> <dd>

Um ponteiro para uma função definida pelo usuário para manipular erros de análise de arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Após o êxito, essa função retorna um ponteiro para uma estrutura [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) . A função **CryptCATCDFEnumAttributesWithCDFTag** retornará um ponteiro **nulo** se falhar.

## <a name="remarks"></a>Comentários

Normalmente, você chama essa função em um loop para enumerar todos os atributos de membro de arquivo de catálogo em um CDF. Antes de entrar no loop, defina *pPrevAttr* como **nulo**. A função retorna um ponteiro para o primeiro atributo. Defina *pPrevAttr* como o valor de retorno da função para iterações subsequentes do loop.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a sequência correta de atribuições para o parâmetro *pPrevAttr* ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

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

[**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
