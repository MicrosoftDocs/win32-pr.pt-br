---
description: Os métodos usados para trabalhar com arquivos DirectX. x podem retornar os valores a seguir, além dos valores de retorno COM padrão. Preterido.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Valores de retorno (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664033"
---
# <a name="return-values-dxfileh"></a>Valores de retorno (DXFile. h)

Os métodos usados para trabalhar com arquivos DirectX. x podem retornar os valores a seguir, além dos valores de retorno COM padrão. Preterido.

<dl> <dt>

<span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ OK**
</dt> <dd>

Comando concluído com êxito.

</dd> <dt>

<span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**DXFILEERR \_ BADALLOC**
</dt> <dd>

Falha na alocação de memória.

</dd> <dt>

<span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**DXFILEERR \_ BADARRAYSIZE**
</dt> <dd>

O tamanho da matriz é inválido.

</dd> <dt>

<span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**DXFILEERR \_ BADCACHEFILE**
</dt> <dd>

O arquivo de cache que contém a data do arquivo. x é inválido. Um arquivo de cache contém dados recuperados da rede, armazenados em cache no disco rígido e recuperados em solicitações subsequentes.

</dd> <dt>

<span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**DXFILEERR \_ BADDataReference**
</dt> <dd>

A referência de dados é inválida.

</dd> <dt>

<span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**DXFILEERR \_ BADFILE**
</dt> <dd>

O arquivo é inválido.

</dd> <dt>

<span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**DXFILEERR \_ BADFILECOMPRESSIONTYPE**
</dt> <dd>

O tipo de compactação de arquivo é inválido.

</dd> <dt>

<span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**DXFILEERR \_ BADFILEFLOATSIZE**
</dt> <dd>

O tamanho do ponto flutuante é inválido.

</dd> <dt>

<span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**DXFILEERR \_ BADFILETYPE**
</dt> <dd>

O arquivo não é um arquivo DirectX. x.

</dd> <dt>

<span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**DXFILEERR \_ BADFILEVERSION**
</dt> <dd>

A versão do arquivo não é válida.

</dd> <dt>

<span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**DXFILEERR \_ BADINTRINSICS**
</dt> <dd>

Intrínsecos são inválidos.

</dd> <dt>

<span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**DXFILEERR \_ BADOBJECT**
</dt> <dd>

Objeto inválido.

</dd> <dt>

<span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**DXFILEERR \_ BADRESOURCE**
</dt> <dd>

O recurso é inválido.

</dd> <dt>

<span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**DXFILEERR \_ BADSTREAMHANDLE**
</dt> <dd>

O identificador de fluxo é inválido.

</dd> <dt>

<span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**DXFILEERR \_ BADTYPE**
</dt> <dd>

O tipo de objeto é inválido.

</dd> <dt>

<span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**DXFILEERR \_ BADVALUE**
</dt> <dd>

O parâmetro é inválido.

</dd> <dt>

<span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**DXFILEERR \_ FILENOTFOUND**
</dt> <dd>

Não foi possível encontrar o arquivo.

</dd> <dt>

<span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**DXFILEERR \_ INTERNALERROR**
</dt> <dd>

Ocorreu um erro interno.

</dd> <dt>

<span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOinternet**
</dt> <dd>

Conexão com a Internet não encontrada.

</dd> <dt>

<span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**DXFILEERR \_ NOMOREDATA**
</dt> <dd>

Não há mais dados disponíveis.

</dd> <dt>

<span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**DXFILEERR \_ NOMOREOBJECTS**
</dt> <dd>

Todos os objetos foram enumerados.

</dd> <dt>

<span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**DXFILEERR \_ NOMORESTREAMHANDLES**
</dt> <dd>

Não há identificadores de fluxo disponíveis.

</dd> <dt>

<span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**DXFILEERR \_ NOTDONEYET**
</dt> <dd>

A operação não foi concluída.

</dd> <dt>

<span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**DXFILEERR não \_ encontrado**
</dt> <dd>

Objeto não encontrado.

</dd> <dt>

<span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR \_ PARSEERROR**
</dt> <dd>

Não foi possível analisar o arquivo.

</dd> <dt>

<span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**DXFILEERR \_ RESOURCENOTFOUND**
</dt> <dd>

Não foi possível encontrar o recurso.

</dd> <dt>

<span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**DXFILEERR \_ NOtemplate**
</dt> <dd>

Nenhum modelo disponível.

</dd> <dt>

<span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**DXFILEERR \_ URLNOTFOUND**
</dt> <dd>

Não foi possível encontrar a URL.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[X referência de arquivo (herdada)](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




