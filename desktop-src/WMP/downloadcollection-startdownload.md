---
title: Método downloadcollection. startDownload
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método startDownload enfileira um download.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- método startDownload Windows Media Player
- método startDownload Windows Media Player, classe Downloadcollection
- Classe downloadcollection Windows Media Player, método startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794488"
---
# <a name="downloadcollectionstartdownload-method"></a>Método downloadcollection. startDownload

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **startDownload** enfileira um download.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sourceURL* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica a URL do download.

</dd> <dt>

*tipo* \[ de no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o tipo de download. Contém um dos seguintes valores.



| Valor      | Descrição                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP e posterior.) O download ocorre como um processo em segundo plano à medida que o tempo do processador se torna disponível. Os Estados de download persistem mesmo quando o Windows Media Player ou o Windows XP é desligado. |
| em tempo real  | (Todos os sistemas operacionais com suporte.) O download ocorre de uma só vez. Nenhum estado de download persiste entre sessões.                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **DownloadItem** .

## <a name="remarks"></a>Comentários

Quando um novo download é iniciado, o Gerenciador de download o adiciona como um item à coleção de download que iniciou o download.

Somente os seguintes formatos de mídia digital podem ser baixados:

-   Advanced Systems Format (ASF)
-   MP3
-   Áudio do Windows Media (WMA)
-   Vídeo do Windows Media (WMV)

O parâmetro *sourceURL* não oferece suporte a cadeias de caracteres codificadas em Unicode. Ele deve apontar para um conteúdo válido. Não há suporte para redirecionamentos.

Ao usar o Windows XP, os arquivos de áudio são colocados automaticamente nas subpastas **minhas músicas** apropriadas com base nos valores de metadados de nível de arquivo. Os arquivos de vídeo são colocados em \\ minha música \\ baixar \\  \\ *tipo* de número aleatório, em que *número aleatório* é um valor aleatório gerado pelo Windows Media Player para cada usuário, e o *tipo* é "real time" ou "background", dependendo do tipo de download.

Ao usar o Windows Media Player 9 Series com o Windows 98 e o Windows Millennium Edition (me), os arquivos de áudio e vídeo são colocados em \\ meu \\ \\ tipo de *número aleatório* de download de música \\ , em que o *número aleatório* é um valor aleatório gerado pelo Player para cada usuário, e o *tipo* é "real time" ou "background", dependendo do tipo de download.

Observe que os arquivos podem ser renomeados com base nos atributos de metadados contidos no arquivo e nas regras especificadas pelo usuário na caixa de diálogo **Opções** . Os arquivos que não contêm metadados, como **álbum** ou **artista**, podem ser movidos para pastas rotuladas como artista desconhecido ou álbum desconhecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto downloadcollection**](downloadcollection-object.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





