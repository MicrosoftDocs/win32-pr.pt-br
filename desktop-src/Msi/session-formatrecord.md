---
description: O método FormatRecord do objeto Session retorna uma cadeia de caracteres formatada de um modelo e registra dados.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Método Session.FormatRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f58aabc0bd222b22ee74cb0b431ce8051ed6bad546d963160c922bd86dee2383
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629146"
---
# <a name="sessionformatrecord-method"></a>Método Session.FormatRecord

O **método FormatRecord** do objeto Session retorna [**uma**](session-object.md) cadeia de caracteres formatada de um modelo e registra dados.

## <a name="syntax"></a>Sintaxe


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Registro* 
</dt> <dd>

Objeto Required **Record** que contém um modelo e dados a serem formatados. A cadeia de caracteres de modelo deve ser definida no campo 0 seguida por quaisquer parâmetros de dados referenciados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O **método FormatRecord** usa o processo de formato a seguir.

Os parâmetros a [serem formatados](formatted.md) são incluídos entre colchetes \[ .. \] . Os colchetes podem ser iterados porque as substituições são resolvidas de dentro para fora.

Se uma parte da cadeia de caracteres estiver entre chaves { } e não contiver colchetes, a parte será deixada inalterada, incluindo as chaves.

Se uma parte da cadeia de caracteres estiver entre chaves e contiver um ou mais nomes de propriedade e se todas as propriedades são encontradas, o texto (com as substituições resolvidas) será exibido sem as chaves. Se qualquer uma das propriedades não for encontrada, todo o texto nas chaves e as chaves em si serão removidos.

**Para formatar cadeias de caracteres usando o método FormatRecord**

1.  Os parâmetros numéricos são substituídos pela substituição do marcador pelo valor do campo de registro correspondente, por valores ausentes ou Nulos que não produzem texto.
2.  A cadeia de caracteres que resulta é processada substituindo os parâmetros que não são de registro pelos valores correspondentes, conforme registrado nas descrições a seguir.
    -   Se uma substring do formato " propertyname " for encontrada, ela será substituída \[ pelo valor da propriedade \] .
    -   Se uma substring do formato " %environmentvariable " for encontrada, o valor da variável de \[ \] ambiente será substituído.
    -   Se uma substring da chave de arquivo de formulário for encontrada, ela será substituída pelo caminho completo do arquivo, pela chave de arquivo de valor usada como uma chave na \[ \#  \] [tabela Arquivo](file-table.md).  O valor de filekey permanece em branco e não é substituído por um caminho até que o instalador executa a ação \[ \#  \] [CostInitialize](costinitialize-action.md), a ação [FileCost](filecost-action.md)e a [ação CostFinalize](costfinalize-action.md). O valor de \[ \# *filekey* \] depende do estado de instalação do componente ao qual o arquivo pertence. Se o componente estiver sendo executado da origem, o valor será o caminho para o local de origem do arquivo. Se o componente estiver sendo executado localmente, o valor será o caminho para o local de destino do arquivo após a instalação. Se o componente estiver ausente, o caminho será em branco. Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte Verificando a [instalação de recursos, componentes, arquivos](checking-the-installation-of-features-components-files.md).
    -   Se uma substring do formulário $componentkey for encontrada, ela será substituída pelo diretório de instalação do componente, pela chave de componente de valor usada como uma chave na \[  \] [tabela Componente](component-table.md).  O valor de componentkey permanece em branco e não é substituído por um diretório até que o instalador executa a ação \[ $  \] [CostInitialize](costinitialize-action.md), a ação [FileCost](filecost-action.md)e a [ação CostFinalize](costfinalize-action.md). O valor de \[ $ *componentkey* \] depende do estado de instalação do componente. Se o componente estiver sendo executado da origem, o valor será o diretório de origem do arquivo. Se o componente estiver sendo executado localmente, o valor será o diretório de destino após a instalação. Se o componente estiver ausente, o valor será deixado em branco. Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte Verificando a [instalação de recursos, componentes, arquivos](checking-the-installation-of-features-components-files.md).
    -   Se uma substring do formato " c " for encontrada, ela será substituída pelo caractere \[ \\ sem nenhum processamento \] posterior. Somente o primeiro caractere após a faixa invertida é mantido; todo o resto é removido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Formatado](formatted.md)
</dt> <dt>

[Tipos de dados de coluna](column-data-types.md)
</dt> </dl>

 

 




