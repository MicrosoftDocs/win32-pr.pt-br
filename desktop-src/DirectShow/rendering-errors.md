---
description: Erros de renderização
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Erros de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456753"
---
# <a name="rendering-errors"></a>Erros de renderização

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O Microsoft® DirectShow® a edição de serviços (DES) define vários códigos de erro usados para registrar erros de renderização. Se um projeto não for renderizado corretamente, o mecanismo de renderização chamará o método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) . A tabela a seguir resume os parâmetros fornecidos para **LogError**:

-   O código de erro está contido no parâmetro *ErrorCode* .
-   A descrição está contida no parâmetro ErrorString.
-   A descrição está contida no parâmetro *ErrorString* .
-   Se houver informações adicionais, o tipo **Variant** estará contido no membro **VT** da **variante** apontada por *pExtraInfo*.

> [!Note]  
> Os códigos de erro descritos aqui não são valores de **HRESULT** . Para obter uma lista de valores de retorno de **HRESULT** específicos do des, consulte [códigos de erro e êxito](error-and-success-codes.md).

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Código do erro</th>
<th>Descrição</th>
<th>Informações adicionais</th>
<th>Tipo de variante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>O nome do arquivo não existe ou o DirectShow não reconhece a extensão do arquivo.</td>
<td>Nome do arquivo</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>O tipo de arquivo não corresponde à extensão do arquivo ou o arquivo está corrompido.</td>
<td>Nome do arquivo</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>O nome do arquivo era necessário, mas não foi fornecido.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>Não é possível analisar a fonte de dados fornecida por essa fonte.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>Erro inesperado. Algum componente do DirectShow não está instalado corretamente.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>O filtro de origem não aceita nomes de arquivo.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>Não há suporte para o tipo de mídia do grupo.</td>
<td>Número do grupo</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>Número de fluxo inválido para esta fonte.</td>
<td>Número do fluxo</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Sem memória.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Um bitmap na sequência não era o mesmo tipo que os outros.</td>
<td>Nome do bitmap</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>Os horários de mídia do clipe são inválidos ou a sequência de DIB (bitmap independente de dispositivo) é muito curta.
<blockquote>
[!Note]<br />
Se outros erros de renderização ocorrerem, esse erro poderá ocorrer mesmo que os horários de mídia sejam válidos.
</blockquote>
<br/></td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>O CLSID (identificador de classe) do efeito ou da transição não é válido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>O CLSID do efeito ou da transição padrão não é válido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>Sua versão do DirectX não oferece suporte a transições tridimensionais.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Esse efeito não é o tipo correto ou está quebrado.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Essa propriedade não existe no objeto.</td>
<td>Nome da propriedade</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Valor ilegal para esta propriedade.</td>
<td>Valor especificado</td>
<td><strong>VARIANTE</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Erro de sintaxe no arquivo XML.</td>
<td>Line number</td>
<td>VT_I4 (inteiro de 4 bytes)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Não é possível encontrar o filtro especificado em XML por categoria e instância.</td>
<td>Nome amigável (instância)</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Erro ao gravar arquivo XML em disco.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID não é um filtro de efeito de áudio do DirectShow válido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Não é possível encontrar um compressor para produzir o formato de compactação especificado.</td>
<td>Nenhum</td>
<td>Não aplicável</td>
</tr>
</tbody>
</table>



 

Os erros a seguir nunca devem ocorrer. Se você encontrar um desses erros, envie um relatório de bugs à Microsoft.



| Código do erro                 | Descrição                                 |
|----------------------------|---------------------------------------------|
| DEX \_ IDs de \_ linha do tempo \_ análise  | Erro inesperado ao analisar a linha do tempo.      |
| \_erro de \_ grafo de IDs Dex \_     | Erro inesperado ao criar o grafo de filtro. |
| \_erro de \_ grade de IDs Dex \_      | Erro inesperado com a grade interna.    |
| \_erro de \_ interface de IDs Dex \_ | Erro inesperado ao obter uma interface.      |



 

 

 




