---
description: 'O WsdCodeGen tem duas funções: geração de arquivos de configuração e geração de código-fonte para aplicativos de cliente e host do WSDAPI.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Sintaxe de linha de comando WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827705"
---
# <a name="wsdcodegen-command-line-syntax"></a>Sintaxe de linha de comando WsdCodeGen

O WsdCodeGen tem duas funções: geração de arquivos de configuração e geração de código-fonte para aplicativos de cliente e host do WSDAPI. Este tópico fornece a sintaxe de linha de comando usada para executar cada tarefa.

## <a name="generating-a-configuration-file"></a>Gerando um arquivo de configuração

### <a name="syntax"></a>Syntax

**WSDCODEGEN.EXE** **/generateconfig:**{host do **cliente** \|  \| **All**} **\[ /OutputFile:**_nome_arquivo_config_ *_\]_* *WSDLFileNameList*

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: {host do cliente \| \| todos}**
</dt> <dd>

O tipo de código que o arquivo de configuração de saída irá gerar. **/generateconfig: o cliente** é usado para gerar um arquivo de configuração para gerar o código do cliente, **/generateconfig: o host** é usado para gerar um arquivo de configuração para gerar o código de host e **/generateconfig: ALL** é usado para gerar um arquivo de configuração para gerar o código do cliente e do host.

</dd> <dt>

<span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/OutputFile:**_nome_arquivo_config_
</dt> <dd>

Esse parâmetro opcional é usado para especificar o nome do arquivo de configuração de saída. Se esse parâmetro for excluído, o nome do arquivo de configuração de saída será codegen.config.

</dd> <dt>

<span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*
</dt> <dd>

Inclua um modelo PnP-X no arquivo de configuração.

</dd> <dt>

<span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*
</dt> <dd>

Uma lista delimitada por espaço dos arquivos WSDL a serem processados pelo WsdCodeGen.

</dd> </dl>

## <a name="generating-source-code"></a>Gerando código-fonte

### <a name="syntax"></a>Syntax

**WSDCODEGEN.EXE** **/GenerateCode** **\[ /Download \]** **\[ /GBC \]** **\[ outputroot:**_caminho_ *_\]_* **\[ /WriteAccess:**_comando_ *_\]_* *nome_arquivo_config*

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**
</dt> <dd>

Direciona o WsdCodeGen para gerar o código-fonte. Esse será o modo padrão se nenhum modo for especificado.

</dd> <dt>

<span id="_download"></span><span id="_DOWNLOAD"></span>**/download**
</dt> <dd>

Baixa documentos importados referenciados pelo arquivo de configuração. Esse parâmetro é opcional.

</dd> <dt>

<span id="_gbc"></span><span id="_GBC"></span>**/gbc**
</dt> <dd>

Adiciona comentários ao código-fonte que indica que o código foi gerado. Esses comentários são prefixados com a frase "gerada por". Esse parâmetro é opcional.

</dd> <dt>

<span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_caminho_
</dt> <dd>

O local de saída para os arquivos gerados. o *caminho* pode ser um caminho absoluto ou relativo. Esse parâmetro é opcional.

</dd> <dt>

<span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/WriteAccess:**_comando_
</dt> <dd>

Direciona o WsdCodeGen para executar o comando especificado antes que ele modifique os arquivos existentes no disco. Os arquivos de saída idênticos àqueles no disco não receberão esse comando, nem eles serão gravados no. Se o comando contiver a sequência " {0} ", essa sequência será substituída pelo nome do arquivo a ser modificado. Caso contrário, o nome do arquivo será anexado ao comando.

Exemplos:

**/WriteAccess: "attrib-r"**

**/WriteAccess: "attrib-r {0} "**

**/WriteAccess: "copiar {0} .. \\ backup \\ "**

</dd> <dt>

<span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nome_arquivo_config*
</dt> <dd>

O nome do arquivo de configuração a ser processado antes de gerar o código.

</dd> </dl>

## <a name="formatting-legend"></a>Legenda de formatação



| Formatar                                                                    | Significado                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| *Itálico*                                                                  | Informações que o usuário deve fornecer                  |
| **Negrito**                                                                  | Elementos devem ser digitados pelo usuário exatamente como mostrados       |
| Entre colchetes ( \[ \] )                                                   | Itens opcionais                                          |
| Entre chaves ( {} ); opções separadas por pipe ( \| ). Exemplo: {par \| ímpar} | Conjunto de opções do qual o usuário deve escolher apenas um |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração WsdCodeGen](wsdcodegen-configuration-file.md)
</dt> <dt>

[Usando WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 




