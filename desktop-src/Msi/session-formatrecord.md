---
description: O método FormatRecord do objeto Session retorna uma cadeia de caracteres formatada de um modelo e dados de registro.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Método Session. FormatRecord
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
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775701"
---
# <a name="sessionformatrecord-method"></a>Método Session. FormatRecord

O método **FormatRecord** do objeto [**Session**](session-object.md) retorna uma cadeia de caracteres formatada de um modelo e dados de registro.

## <a name="syntax"></a>Sintaxe


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*gravável* 
</dt> <dd>

Objeto de **registro** necessário contendo um modelo e dados a serem formatados. A cadeia de caracteres do modelo deve ser definida no campo 0 seguido por quaisquer parâmetros de dados referenciados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método **FormatRecord** usa o seguinte processo de formato.

Os parâmetros a serem [formatados](formatted.md) são colocados entre colchetes \[ .. \] . Os colchetes podem ser iterados porque as substituições são resolvidas de dentro para fora.

Se uma parte da cadeia de caracteres estiver entre chaves {} e não contiver colchetes, a parte permanecerá inalterada, incluindo as chaves.

Se uma parte da cadeia de caracteres estiver entre chaves e contiver um ou mais nomes de propriedade, e se todas as propriedades forem encontradas, o texto (com as substituições resolvidas) será exibido sem as chaves. Se qualquer uma das propriedades não for encontrada, todo o texto entre chaves e as chaves serão removidos.

**Para formatar Cadeias de caracteres usando o método FormatRecord**

1.  Os parâmetros numéricos são substituídos substituindo o marcador pelo valor do campo de registro correspondente, com valores ausentes ou nulos que não produzem nenhum texto.
2.  A cadeia de caracteres que resulta é processada substituindo os parâmetros que não são de registro pelos valores correspondentes, conforme observado nas descrições a seguir.
    -   Se uma subcadeia de caracteres do formato " \[ PropertyName \] " for encontrada, ela será substituída pelo valor da propriedade.
    -   Se uma subcadeia de caracteres do formulário " \[ % environmentvariable \] " for encontrada, o valor da variável de ambiente será substituído.
    -   Se uma subcadeia de caracteres do formulário \[ \# *FileKey* \] for encontrada, ela será substituída pelo caminho completo do arquivo, com o valor *FileKey* usado como uma chave na [tabela de arquivos](file-table.md). O valor de \[ \# *FileKey* \] permanece em branco e não é substituído por um caminho até que o instalador execute a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md). O valor de \[ \# *FileKey* \] depende do estado da instalação do componente ao qual o arquivo pertence. Se o componente estiver sendo executado da origem, o valor será o caminho para o local de origem do arquivo. Se o componente estiver sendo executado localmente, o valor será o caminho para o local de destino do arquivo após a instalação. Se o componente estiver ausente, o caminho ficará em branco. Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte [verificando a instalação de recursos, componentes e arquivos](checking-the-installation-of-features-components-files.md).
    -   Se uma subcadeia de caracteres do formulário \[ *$componentkey* \] for encontrada, ela será substituída pelo diretório de instalação do componente, com o valor *componentkey* usado como uma chave na [tabela de componentes](component-table.md). O valor de \[ $ *componentkey* \] permanece em branco e não é substituído por um diretório até que o instalador execute a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md). O valor de \[ $ *componentkey* \] depende do estado de instalação do componente. Se o componente estiver sendo executado da origem, o valor será o diretório de origem do arquivo. Se o componente estiver sendo executado localmente, o valor será o diretório de destino após a instalação. Se o componente estiver ausente, o valor será deixado em branco. Para obter mais informações sobre como verificar o estado de instalação dos componentes, consulte [verificando a instalação de recursos, componentes e arquivos](checking-the-installation-of-features-components-files.md).
    -   Se uma subcadeia de caracteres no formato " \[ \\ c \] " for encontrada, ela será substituída pelo caractere sem nenhum processamento adicional. Somente o primeiro caractere após a barra invertida é mantido; Tudo o mais é removido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Binário](formatted.md)
</dt> <dt>

[Tipos de dados de coluna](column-data-types.md)
</dt> </dl>

 

 




