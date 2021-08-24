---
description: cria um novo catálogo personalizado no indexador Windows pesquisa e retorna uma referência a ele.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'Método ISearchManager2:: createcatalog'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 34a4ceb37045ebbae62e04da0b5395673ed498c56189a26f2abaa376c960c511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597746"
---
# <a name="isearchmanager2createcatalog-method"></a>Método ISearchManager2:: createcatalog

cria um novo catálogo personalizado no indexador Windows pesquisa e retorna uma referência a ele.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszCatalog* \[ no\]
</dt> <dd>

Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Nome do catálogo a ser criado. Pode ser qualquer nome selecionado pelo chamador, deve conter apenas caracteres alfanuméricos padrão e sublinhado.

</dd> <dt>

*ppCatalogManager* \[ fora\]
</dt> <dd>

Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

Em caso de sucesso, uma referência ao catálogo criado é retornada como um ponteiro de interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . A versão () deve ser chamada nesta interface depois que o aplicativo de chamada terminar de usá-la.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

HRESULT indicando o status da operação:



| Código de retorno                                                                             | Descrição                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O catálogo não existia e foi criado anteriormente. Referência ao catálogo retornada.<br/> |
| <dl> <dt>**\_falso**</dt> </dl> | O catálogo já existia, referência ao catálogo retornada.<br/>                       |



 

HRESULT com falha: falha ao criar catálogo ou argumentos inválidos passados.

## <a name="remarks"></a>Comentários

chamado para criar um novo catálogo no indexador de pesquisa Windows. Após a criação, os métodos no Gerenciador de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) retornado podem ser usados para adicionar locais a serem indexados, monitorar o processo de indexação e construir consultas para enviar ao indexador e obter resultados. Consulte a documentação "Gerenciando o índice" para obter mais informações: https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
