---
description: Erros de renderização
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Erros de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31d49c5fbb82457282decdaa07152e75db6bc3e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482582"
---
# <a name="rendering-errors"></a>Erros de renderização

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Microsoft® DirectShow® DES (Serviços de Edição) define vários códigos de erro usados para registrar erros de renderização. Se um projeto não renderizar corretamente, o mecanismo de renderização chamará o [**método IAMErrorLog::LogError.**](iamerrorlog-logerror.md) A tabela a seguir resume os parâmetros dados a **LogError:**

-   O código de erro está contido no *parâmetro ErrorCode.*
-   A descrição está contida no parâmetro ErrorString.
-   A descrição está contida no *parâmetro ErrorString.*
-   Se houver informações adicionais, o **tipo VARIANT** será contido no **membro vt** **da VARIANT** apontado por *pExtraInfo*.

> [!Note]  
> Os códigos de erro descritos aqui não são **valores HRESULT.** Para ver uma lista de **valores de retorno HRESULT** específicos ao DES, consulte [Códigos de erro e êxito.](error-and-success-codes.md)

 




| Código do erro | Descrição | Informações adicionais | Tipo de variante | 
|------------|-------------|-------------------|--------------|
| DEX_IDS_BAD_SOURCE_NAME | O nome do arquivo não existe ou DirectShow não reconhece a extensão de arquivo. | Nome do arquivo | <strong>BSTR</strong> | 
| DEX_IDS_BAD_SOURCE_NAME2 | O tipo de arquivo não corresponderá à extensão de arquivo ou o arquivo está corrompido. | Nome do arquivo | <strong>BSTR</strong> | 
| DEX_IDS_MISSING_SOURCE_NAME | O nome do arquivo era necessário, mas não foi dado. | Nenhum | Não aplicável | 
| DEX_IDS_UNKNOWN_SOURCE | Não é possível analisar a fonte de dados fornecida por essa fonte. | Nenhum | Não aplicável | 
| DEX_IDS_INSTALL_PROBLEM | Erro inesperado. Alguns DirectShow componente não estão instalados corretamente. | Nenhum | Não aplicável | 
| DEX_IDS_NO_SOURCE_NAMES | O filtro de origem não aceita nomes de arquivo. | Nenhum | Não aplicável | 
| DEX_IDS_BAD_MEDIATYPE | Não há suporte para o tipo de mídia do grupo. | Número do grupo | <strong>int</strong> | 
| DEX_IDS_STREAM_NUMBER | Número de fluxo inválido para essa origem. | Número do fluxo | <strong>int</strong> | 
| DEX_IDS_OUTOFMEMORY | Sem memória. | Nenhum | Não aplicável | 
| DEX_IDS_DIBSEQ_NOTALLSAME | Um bitmap na sequência não era do mesmo tipo que os outros. | Nome do bitmap | <strong>BSTR</strong> | 
| DEX_IDS_CLIPTOOSHORT | Os tempos de mídia do clipe são inválidos ou a sequência DIB (bitmap independente de dispositivo) é muito curta.<blockquote>[!Note]<br />Se ocorrerem outros erros de renderização, esse erro poderá ocorrer mesmo que os tempos de mídia sejam válidos.</blockquote><br /> | Nenhum | Não aplicável | 
| DEX_IDS_INVALID_DXT | O CLSID (identificador de classe) do efeito ou da transição não é válido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_INVALID_DEFAULT_DXT | O CLSID do efeito padrão ou da transição não é válido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_3D | Sua versão do DirectX não dá suporte a transições tridimensionais. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_BROKEN_DXT | Esse efeito não é do tipo certo ou está desfeito. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_SUCH_PROPERTY | Essa propriedade não existe no objeto . | Nome da propriedade | <strong>BSTR</strong> | 
| DEX_IDS_ILLEGAL_PROPERTY_VAL | Valor ilegal para essa propriedade. | Valor especificado | <strong>VARIANTE</strong> | 
| DEX_IDS_INVALID_XML | Erro de sintaxe no arquivo XML. | Line number | VT_I4 (inteiro de 4 byte) | 
| DEX_IDS_CANT_FIND_FILTER | Não é possível encontrar o filtro especificado em XML por categoria e instância. | Nome amigável (instância) | <strong>BSTR</strong> | 
| DEX_IDS_DISK_WRITE_ERROR | Erro ao escrever arquivo XML no disco. | Nenhum | Não aplicável | 
| DEX_IDS_INVALID_AUDIO_FX | CLSID não é um filtro de DirectShow de efeito de áudio válido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_CANT_FIND_COMPRESSOR | Não é possível encontrar um compressor para produzir o formato de compactação especificado. | Nenhum | Não aplicável | 




 

Os erros a seguir nunca devem ocorrer. Se você encontrar um desses erros, envie um relatório de bugs à Microsoft.



| Código do erro                 | Descrição                                 |
|----------------------------|---------------------------------------------|
| DEX \_ IDs de \_ linha do tempo \_ análise  | Erro inesperado ao analisar a linha do tempo.      |
| \_erro de \_ grafo de IDs Dex \_     | Erro inesperado ao criar o grafo de filtro. |
| \_erro de \_ grade de IDs Dex \_      | Erro inesperado com a grade interna.    |
| \_erro de \_ interface de IDs Dex \_ | Erro inesperado ao obter uma interface.      |



 

 

 




