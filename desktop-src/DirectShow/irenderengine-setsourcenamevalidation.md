---
description: O método SetSourceNameValidation especifica como o mecanismo de renderização valida nomes de arquivo.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'Método IRenderEngine:: SetSourceNameValidation (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757011"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a>Método IRenderEngine:: SetSourceNameValidation

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetSourceNameValidation` método especifica como o mecanismo de renderização valida nomes de arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FilterString* 
</dt> <dd>

Valor **BSTR** que contém pares de cadeias de caracteres de filtro, formatados conforme exigido pelo membro **LpstrFilter** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . O localizador de mídia usará esse filtro se ele apresentar uma caixa de diálogo abrir arquivo ao usuário final.

</dd> <dt>

*pOverride* 
</dt> <dd>

Ponteiro opcional para a interface [**IMediaLocator**](imedialocator.md) de um localizador de mídia a ser usado no lugar do padrão. Para usar o localizador de mídia padrão, defina o valor desse parâmetro como **NULL**. Consulte comentários para obter mais informações.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Combinação de bits bit de [**sinalizadores de validação de nome de arquivo**](file-name-validation-flags.md) especificando o comportamento do localizador de mídia. O sinalizador de verificação de VALIDATEF de SFN \_ \_ deve estar presente. O \_ sinalizador SFN VALIDATEF \_ hlinkMUTED não tem nenhum efeito com esse método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl> | Falha ao inicializar o mecanismo de renderização.<br/> |



 

## <a name="remarks"></a>Comentários

Usando o parâmetro *pOverride* , você pode fornecer sua própria implementação personalizada da interface [**IMediaLocator**](imedialocator.md) . Por exemplo, o localizador de mídia padrão não notifica um aplicativo sobre os arquivos que ele encontra (ou não pode localizar). Para contornar essa limitação, você pode implementar um localizador de mídia personalizado, tornando-o um wrapper para a versão padrão. Em seguida, passe [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) chamadas diretamente para a versão padrão e examine o valor de retorno.

Atualmente, esse método não valida as fontes carregadas dinamicamente. Consulte [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 
