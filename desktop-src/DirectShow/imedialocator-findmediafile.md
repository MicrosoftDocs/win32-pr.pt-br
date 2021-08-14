---
description: O método FindMediaFile pesquisa um arquivo e, se bem-sucedido, recupera o caminho para o arquivo.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: Método IMediaLocator::FindMediaFile (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc1acda4a3bc6e2d93ae8b7024ef34f759c11c5c4d487a09d3be3a3542e0c445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818933"
---
# <a name="imedialocatorfindmediafile-method"></a>Método IMediaLocator::FindMediaFile

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `FindMediaFile` método pesquisa um arquivo e, se bem-sucedido, recupera o caminho para o arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Entrada* 
</dt> <dd>

Nome do arquivo, incluindo caminho, em que o arquivo era conhecido por residir pela última vez. Para objetos de origem na linha do tempo, use o nome da mídia atual.

</dd> <dt>

*FilterString* 
</dt> <dd>

Uma **BSTR que** contém pares de cadeias de caracteres de filtro, formatadas conforme exigido pelo membro **lpstrFilter** da [**estrutura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) O localizador de mídia usará esse filtro se exibir uma caixa de diálogo Abrir Arquivo. O valor poderá ser **NULL se** o *parâmetro Flags* não incluir o sinalizador \_ POPUP SFN \_ VALIDATEF.

</dd> <dt>

*pOutput* 
</dt> <dd>

Ponteiro para uma variável que recebe o caminho real para o arquivo, se ele for diferente do valor contido em *Entrada* e se o método localizar o arquivo com êxito.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Combinação bit a bit de zero ou mais sinalizadores. Para ver uma lista de possíveis sinalizadores, consulte [**Sinalizadores de validação de nome de arquivo**](file-name-validation-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

A cadeia de caracteres de filtro para a caixa de diálogo Arquivo Aberto, que é especificada pelo *parâmetro FilterString,* contém caracteres Nulos internos. Por exemplo, Vídeo \\ 0 \*.avi\\ 0 \\ 0 é uma cadeia de caracteres de filtro válida. Você não pode usar a função **SysAllocStr** para alocar o BSTR, porque essa função espera uma cadeia de caracteres terminada em nulo e truncará a cadeia de caracteres no primeiro caractere Nulo. Portanto, use uma função como **SysAllocStringLen**, que inclui um parâmetro explícito para o comprimento:


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



Se o usuário cancelar a caixa de diálogo Abrir Arquivo, o método retornará E \_ FAIL.

O método aloca memória para o **BSTR** em *pOutput.* O aplicativo deve chamar **SysFreeString** para liberar a memória.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaLocator Interface**](imedialocator.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 
