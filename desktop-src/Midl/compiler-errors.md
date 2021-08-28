---
title: Erros do Compilador
description: Lista de mensagens de erro geradas durante a compilação MIDL.
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- erros MIDL, erros do compilador
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04bfb8f3465849215711ff70b9d9d67e40817f4e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884610"
---
# <a name="compiler-errors"></a>Erros do Compilador

As seguintes mensagens de erro são geradas durante a compilação MIDL:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Código de retorno</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>deve especificar /c_ext declaradores abstratos</dt> <dd> Declaradores abstratos representam uma extensão da Microsoft para RPC e não são definidos no DCE RPC. Portanto, se o arquivo incluir declaradores abstratos, você não poderá compilar com a opção <a href="-osf.md"><strong>/osf,</strong></a> que impõe compatibilidade de DCE estrita. As versões MIDL 3.0 e posteriores usam a <a href="-c-ext.md"><strong>opção /c_ext</strong></a> como o padrão; a <strong>opção /osf</strong> desliga a <strong>opção /c_ext.</strong> Para obter informações sobre declaradores abstratos, consulte <a href="/windows/desktop/Rpc/the-acf-body">The ACF Body</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>a insta instação de dados é ilegal; você deve usar &quot; extern &quot; ou &quot; estático&quot;</dt> <dd> A declaração e a inicialização no arquivo IDL não são compatíveis com o DCE RPC. Esse recurso é uma extensão da Microsoft que não está disponível quando você compila no modo de compatibilidade com DCE (<a href="-osf.md"><strong>/osf).</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>estouro de pilha do compilador</dt> <dd> O compilador ficou sem espaço na pilha durante o processamento do arquivo IDL. Esse problema pode ocorrer quando o compilador está processando uma declaração ou expressão complexa. Para resolver o problema, simplifique a declaração ou expressão complexa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>Redefinição</dt> <dd> Essa mensagem de erro pode aparecer nas seguintes circunstâncias: um tipo foi redefinido; um protótipo de procedimento foi redefinido; já existe um membro de uma estrutura ou união com o mesmo nome; já existe um parâmetro com o mesmo nome no protótipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>[auto_handle] a associação será usada</dt> <dd> Nenhum tipo de identificador foi definido como o tipo de identificador padrão. O compilador presume que um alça automática será usado como o alça de associação para o procedimento especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>memória fora de memória</dt> <dd> O compilador ficou sem memória durante a compilação. Reduza o tamanho ou a complexidade do arquivo IDL ou aloce mais memória ao processo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>definição recursiva</dt> <dd> Uma estrutura ou união foi definida recursivamente. Esse erro pode ocorrer quando uma especificação de ponteiro em uma definição de estrutura aninhada é perdida.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>importação ignorada; arquivo já importado</dt> <dd> Importar um arquivo IDL é uma operação idempotente. Incluí-lo mais de uma vez não tem nenhum efeito. Todos, menos a primeira operação de importação, são ignorados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>As enums esparsas exigem /c_ext ou /ms_ext</dt> <dd> Atribuir valores a constantes de enumeração não é compatível com DCE RPC. Se você quiser usar as extensões da Microsoft para MIDL que permitem atribuir valores a constantes de enumeração, não será possível compilar com a opção <a href="-osf.md"><strong>/osf,</strong></a> que impõe a compatibilidade de DCE estrita. As versões MIDL 3.0 e posteriores usam as opções <a href="-c-ext.md"><strong>/c_ext</strong></a> <a href="-ms-ext.md"><strong>e /ms_ext como</strong></a> padrão; a <strong>opção /osf</strong> desliga essas opções de extensão.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>Símbolo indefinido</dt> <dd> Um símbolo indefinido foi usado em uma expressão. Esse erro pode ocorrer quando você usa um valor enumerado indefinido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>tipo usado no arquivo ACF não definido no arquivo IDL</dt> <dd> Um tipo indefinido está sendo usado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>Declaração de tipo não resolvida</dt> <dd> O tipo relatado no campo de informações de erro adicional não foi definido em outro lugar no arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>O uso de constantes de caractere largo requer /ms_ext ou /c_ext</dt> <dd> Constantes de caractere largo são uma extensão da Microsoft para ADL de DCE. Para usar o tipo de <a href="wchar-t.md"><strong>dados wchar_t</strong></a>, não é possível compilar com a opção <a href="-osf.md"><strong>/osf,</strong></a> que substitui as opções padrão do compilador MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> e <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>O uso de cadeias de caracteres largos requer /ms_ext ou /c_ext</dt> <dd> Constantes de cadeia de caracteres largos são uma extensão da Microsoft para ADL de DCE. Para usar o tipo de <a href="wchar-t.md"><strong>dados wchar_t</strong></a>, não é possível compilar com a opção <a href="-osf.md"><strong>/osf,</strong></a> que substitui as opções padrão do compilador MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> e <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>redefinição inconsistente do tipo wchar_t</dt> <dd> O tipo <a href="wchar-t.md"><strong>wchar_t</strong></a> foi redefinido como um tipo que não é equivalente ao DOS curto sem assinatura *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>importlib não encontrado</dt> <dd> O compilador não pôde encontrar a biblioteca de tipos especificada pela diretiva [ <a href="importlib.md"><strong>importlib</strong></a>]. Verifique se o caminho e o nome da biblioteca estão corretos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>dois blocos de biblioteca</dt> <dd> Dois blocos de biblioteca (mesmo com nomes diferentes) no mesmo arquivo de origem são ilícitos. Combine todos os elementos em um único bloco de biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>a instrução dispinterface requer uma definição para IDispatch</dt> <dd> Esse erro geralmente ocorre quando os arquivos Stdole2.tlb ou O meio-dial.idl não são importados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>erro ao acessar a biblioteca de tipos</dt> <dd> O compilador não pôde encontrar a biblioteca de tipos especificada. Verifique se você especificou o caminho corretamente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>erro ao acessar informações de tipo</dt> <dd> A biblioteca de tipos importada está corrompida, inválida ou apenas parcialmente construída.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>erro ao gerar a biblioteca de tipos</dt> <dd> Não foi possível gerar a biblioteca de tipos. Uma possível causa desse erro é especificar um caminho para o arquivo IDL com mais de 126 caracteres. Oleaut32.dll não dá suporte a nomes de caminho com mais de 126 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>ID duplicada</dt> <dd> Os aplicativos usam <a href="id.md"><strong>a instrução id</strong></a> em arquivos IDL para especificar um DISPID para funções membro. As funções membro podem ser propriedades ou métodos de interfaces ou dispinterfaces. Esse erro indica que o arquivo IDL especifica o mesmo número de identificador para dois métodos ou propriedades.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>Valor ilegal ou ausente para o atributo de entrada</dt> <dd> O argumento para o atributo de entrada pode ser uma cadeia de caracteres que especifica um ponto de entrada nomeado ou um número ordinal que define o ponto de entrada. Esse argumento está ausente ou contém um valor inválido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>a recuperação de erro assume</dt> <dd> O compilador MIDL encontrou caracteres ilícitos no arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>descartes de recuperação de erro</dt> <dd> O compilador MIDL encontrou caracteres ilícitos no arquivo IDL. Ele ignorará os caracteres ilícitos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>erro de sintaxe</dt> <dd> O compilador detectou um erro de sintaxe na linha especificada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>não pode se recuperar de erros de sintaxe anteriores; anulando a compilação</dt> <dd> O compilador MIDL tenta se recuperar automaticamente de erros de sintaxe adicionando ou removendo elementos sintáticos. Essa mensagem indica que, apesar dessas tentativas de recuperação, o compilador detectou muitos erros. Corrija os erros especificados e recompile.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>opção pragma desconhecida</dt> <dd> Não há suporte para o pragma C especificado em MIDL. Remova o pragma do arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>recurso não implementado</dt> <dd> O recurso MIDL, embora faça parte da definição de linguagem, não é implementado no Microsoft RPC e não é suportado pelo compilador MIDL. Por exemplo, os seguintes recursos de linguagem não são implementados: bitset, pipe e o tipo de caractere internacional. O recurso de idioma não simplificado aparece no campo adicional de informações de erro da mensagem de erro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>tipo não implementado</dt> <dd> O tipo de dados especificado, embora seja uma palavra-chave MIDL legal, não é implementado no Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>não ponteiro usado em uma operação de desreferência</dt> <dd> Um tipo de dados que não é um ponteiro foi associado a operações de ponteiro. Não é possível acessar o objeto por meio do ponteiro não especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>expression tem uma divisão por zero</dt> <dd> A expressão constante contém divisão por zero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>expression usa tipos incompatíveis</dt> <dd> Os lados esquerdo e direito do operador em uma expressão são de tipos incompatíveis.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>A expressão nonarray usa o operador de índice</dt> <dd> A expressão usa a operação de indexação de matriz em um item de dados que não é do tipo de matriz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>o lado esquerdo da expressão não é avaliada como struct/union/enum</dt> <dd> O operador de referência direta ou indireta . ou foi aplicado a um objeto de dados que não é uma estrutura, uma união &quot; &quot; ou uma &quot; -> &quot; enumeração. Você não pode obter uma referência direta ou indireta usando o objeto especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>expressão constante esperada</dt> <dd> Uma expressão constante era esperada na sintaxe. Por exemplo, os limites de matriz exigem uma expressão constante. O compilador emite essa mensagem de erro quando o limite da matriz é definido com uma variável ou símbolo indefinido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>A expressão não pode ser avaliada no tempo de compilação</dt> <dd> O compilador não pode avaliar uma expressão em tempo de compilação.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>expressão não implementada</dt> <dd> Não há suporte para um recurso com suporte em versões anteriores do compilador MIDL na versão do compilador fornecida com o Microsoft RPC. Remova a expressão especificada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>nenhum atributo [pointer_default] especificado, supondo que [exclusivo] para todos os ponteiros não atribuídos</dt> <dd> O compilador MIDL oferece três casos padrão diferentes para ponteiros que não têm atributos de ponteiro. Os parâmetros de função que são ponteiros de nível superior assumem como padrão [<a href="ref.md"><strong>ref</strong></a>] ponteiros. Os ponteiros inseridos em estruturas e ponteiros para outros ponteiros (não ponteiros de nível superior) são padrão para o tipo especificado pelo atributo [<a href="pointer-default.md"><strong>pointer_default</strong></a>] . Quando nenhum atributo [<strong>pointer_default</strong>] é fornecido, esses ponteiros de nível não superior assumem como padrão ponteiros exclusivos. Esta mensagem de erro indica o último caso: nenhum atributo [<strong>pointer_default</strong>] é fornecido e há pelo menos um ponteiro não de nível superior que será tratado como um ponteiro exclusivo. Para obter mais informações, consulte <a href="/windows/desktop/Rpc/default-pointer-types">Tipos de ponteiro padrão</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>interface não é compatível com marshaling de automação</dt> <dd> A interface não atendem aos requisitos de uma interface de Automação OLE. Verifique se a interface é derivada de <strong>IUnknown</strong> ou <strong>IDispatch</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] Somente o parâmetro não pode ser um ponteiro para uma estrutura aberta</dt> <dd> Um parâmetro [<a href="out-idl.md"><strong>out</strong></a>]-only foi usado como um ponteiro para uma estrutura, conhecida como uma estrutura aberta, cujo intervalo e tamanho transmitidos são determinados em tempo de executar. O stub do servidor não sabe quanto espaço alocar para uma estrutura aberta. Use um ponteiro para um ponteiro para a estrutura aberta e verifique se o aplicativo de servidor aloca espaço suficiente para ele.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] Somente o parâmetro não pode ser uma cadeia de caracteres não localizada</dt> <dd> Uma matriz com o atributo de cadeia de caracteres foi declarada como um parâmetro [<a href="out-idl.md"><strong>out</strong></a>]-only sem qualquer especificação de tamanho. O stub do servidor precisa de informações de tamanho para alocar memória para a cadeia de caracteres. Você pode remover o atributo de cadeia de caracteres e adicionar o atributo [<a href="size-is.md"><strong>size_is</strong></a>] ou pode alterar o parâmetro para um parâmetro [<strong>in, out</strong>] .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>O parâmetro [out] não é um ponteiro</dt> <dd> Todos os<a href="out-idl.md"><strong>parâmetros</strong></a>[ out ] devem ser ponteiros, de acordo com a convenção de chamada por valor da linguagem de programação C. O parâmetro<strong>direcional</strong>[ out ] indica que o servidor transmite um valor para o cliente. Com a convenção de chamada por valor, o servidor poderá transmitir dados para o cliente somente se o argumento de função for um ponteiro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>a estrutura aberta não pode ser um parâmetro</dt> <dd> Uma estrutura aberta contém uma matriz compatível como o último elemento. Uma estrutura ou união é truncada quando o último elemento dessa estrutura ou união é uma matriz compatível.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] identificador de contexto/identificador genérico deve ser especificado como um ponteiro para esse tipo de identificador</dt> <dd> Um parâmetro de alça de contexto ou de alça definido pelo usuário com o atributo direcional [<a href="out-idl.md"><strong>out</strong></a>] deve ser um ponteiro para um ponteiro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>O identificador de contexto não deve derivar de um tipo que tenha o atributo [transmit_as]</dt> <dd> Os alças de contexto devem ser transmitidos como tipos de alça de contexto. Eles não podem ser transmitidos como outros tipos e não podem derivar de [transmit_is], [<strong>represent_as</strong>], [<strong>wire_marshal</strong>], ou [<strong>user_marshal</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>não pode especificar um número variável de argumentos para um procedimento remoto</dt> <dd> Chamadas de procedimento remoto que especificam um número variável de argumentos em tempo de compilação não são compatíveis com a definição de RPC de DCE. Não é possível usar um número variável de argumentos no Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>o parâmetro nomeado não pode ser &quot; nulo&quot;</dt> <dd> Um parâmetro com o tipo base <a href="void.md"><strong>void</strong></a> é especificado com um nome.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>O parâmetro deriva de &quot; coclass &quot; ou &quot; módulo&quot;</dt> <dd> A <a href="coclass.md"><strong>coclasse</strong></a> especifica um objeto de nível superior que contém interfaces e dispinterfaces. Ele não pode ser passado como um parâmetro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>somente o primeiro parâmetro pode ser um alça de associação; você deve especificar a opção /ms_ext</dt> <dd> O DCE RPC permite que apenas o primeiro parâmetro seja um alça de associação. Compilar com a opção <a href="-osf.md"><strong>/osf</strong></a> desliga a opção <a href="-ms-ext.md"><strong>/ms_ext</strong></a> padrão que dá suporte a vários parâmetros de alça e manipular parâmetros em diferentes da posição mais à esquerda.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>não pode usar [comm_status] em um parâmetro e um tipo de retorno</dt> <dd> O procedimento e um de seus parâmetros têm o atributo [<a href="comm-status.md"><strong>comm_status</strong></a>] . O atributo [<strong>comm_status</strong>] especifica que apenas um objeto de dados por vez pode ser do <a href="error-status-t.md"><strong>tipo error_status_t</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> O atributo [local] em um procedimento requer /ms_ext</dt> <dd> O atributo [<a href="local.md"><strong>local</strong></a>] é uma extensão da Microsoft para ADL de DCE. Para usar esse atributo em uma função, não é possível compilar com a <a href="-osf.md"><strong>opção /osf.</strong></a> A <strong>opção /osf</strong> substitui as opções padrão do compilador MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> <a href="-c-ext.md"><strong>e /c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>atributos de propriedade só podem ser usados com procedimentos</dt> <dd> Uso inadequado de um atributo [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>], ou [<a href="propputref.md"><strong>propputref</strong></a>]. Verifique se você escreveu o nome da função da propriedade corretamente e se a propriedade e a função têm o mesmo nome.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>um procedimento pode não ter mais de um atributo de propriedade</dt> <dd> No máximo, apenas um dos atributos [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>], ou [<a href="propputref.md"><strong>propputref</strong></a>] pode ser especificado para uma função.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>o procedimento tem uma combinação ilegal de atributos de operação</dt> <dd> Determinados atributos não podem ser usados em conexão com outros atributos. Verifique a Referência da Linguagem MIDL para ver os requisitos exatos e a sintaxe dos atributos usados neste procedimento.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>O campo que deriva de uma matriz compatível deve ser o último membro da estrutura</dt> <dd> A estrutura contém uma matriz compatível que não é o último elemento na estrutura. A matriz compatível deve aparecer como o último elemento de estrutura.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>duplicar [caso] rótulo</dt> <dd> Um rótulo de caso duplicado foi especificado. O rótulo duplicado é exibido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>nenhum caso [padrão] especificado para união discriminada</dt> <dd> Uma união discriminada foi especificada sem um caso padrão.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>A expressão de atributo não pode ser resolvida</dt> <dd> A expressão associada ao atributo não pode ser resolvida. Esse erro geralmente ocorre quando uma variável que aparece na expressão não é definida. Por exemplo, o erro pode ocorrer quando a variável <em>s</em> não está definida e é usada pelo atributo [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>A expressão de atributo deve ser do tipo integral, sem suporte para expressões de 64 bits</dt> <dd> A variável de atributo ou expressão especificada deve ser um tipo integral. Esse erro ocorre quando o tipo de expressão de atributo não é resolvido para um inteiro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] requer /ms_ext</dt> <dd> O atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] é uma extensão da Microsoft para ADL de DCE. Para usar esse atributo, não é possível compilar com a opção <a href="-osf.md"><strong>/osf,</strong></a> que substitui as opções padrão do compilador MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> e <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] pode ser aplicado somente a parâmetros de saída do tipo de ponteiro</dt> <dd> O atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] só pode ser aplicado aos parâmetros [<a href="out-idl.md"><strong>out</strong></a>] e todos os parâmetros [<strong>out</strong>] devem ser tipos de ponteiro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] não pode ser especificado em um ponteiro para uma matriz ou estrutura compatível</dt> <dd> O atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] não pode ser aplicado a uma matriz ou estrutura compatível.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>parâmetro que especifica que a contagem de byte não é [in] somente ou o parâmetro de contagem de byte não é somente [out]</dt> <dd> O valor associado ao [<a href="byte-count.md"><strong>byte_count</strong></a>] deve ser transmitido do cliente para o servidor; ele deve ser um parâmetro [<a href="in.md"><strong>em</strong></a>] . O parâmetro [<strong>byte_count</strong>] não precisa ser um parâmetro [<strong>in, out</strong>] .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>parâmetro que especifica que a contagem de byte não é um tipo integral</dt> <dd> O valor associado à contagem de byte deve ser o tipo inteiro <a href="int.md"><strong>int,</strong></a> <a href="small.md"><strong>pequeno,</strong></a> <a href="short.md"><strong>curto</strong></a>ou <a href="long.md"><strong>longo.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] não pode ser especificado em um parâmetro com atributos de tamanho</dt> <dd> O atributo [<a href="byte-count.md"><strong>byte_count</strong></a>] não pode ser usado com outros atributos de tamanho, como [<a href="size-is.md"><strong>size_is</strong></a>] ou [<a href="length-is.md"><strong>length_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>A expressão [case] não é constante</dt> <dd> A expressão especificada para o rótulo de caso não é uma constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>A expressão [case] não é do tipo integral</dt> <dd> A expressão especificada para o rótulo de caso não é um tipo inteiro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>especificar [context_handle] em um tipo diferente de void * requer /ms_ext</dt> <dd> Para compatibilidade com DCE-RPC, o identificador de contexto deve ser um ponteiro do tipo <strong>void *</strong>. Se você quiser que os alças de contexto sejam associados a tipos diferentes de <strong>void *</strong>, não use a opção <a href="-osf.md"><strong>/osf</strong></a>do compilador MIDL, que substitui a opção padrão do compilador MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>não pode especificar mais de um parâmetro com cada um dos comm_status/fault_status</dt> <dd> Um procedimento pode ter apenas um parâmetro com o atributo [<a href="comm-status.md"><strong>comm_status</strong></a>] . Ele pode ter no máximo um parâmetro com o atributo [<a href="fault-status.md"><strong>fault_status</strong></a>] .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>comm_status/fault_status deve ser um parâmetro de ponteiro somente [out]</dt> <dd> Os tipos de código de erro [<a href="comm-status.md"><strong>comm_status</strong></a>] e [<a href="fault-status.md"><strong>fault_status</strong></a>] são transmitidos do servidor para o cliente e, portanto, devem ser especificados como um parâmetro [<a href="out-idl.md"><strong>out</strong></a>] . Devido às restrições na linguagem de programação C, todos os parâmetros [<strong>out</strong>] devem ser ponteiros.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>erro de sintaxe do ponto de extremidade</dt> <dd> A sintaxe do ponto de extremidade está incorreta.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>atributo inaplicável</dt> <dd> O atributo especificado não pode ser aplicado neste constructo. Por exemplo, o atributo de cadeia de caracteres se aplica a <a href="char-idl.md"><strong>matrizes</strong></a> char ou ponteiros <strong>char</strong> e não pode ser aplicado a uma estrutura que consiste em dois <a href="short.md"><strong>inteiros</strong></a> curtos: <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[allocate] requer /ms_ext</dt> <dd> O <a href="allocate.md"><strong>atributo allocate</strong></a> representa uma extensão da Microsoft que não está definida como parte do DCE RPC. Para usar esse atributo, não é possível compilar com a opção <a href="-osf.md"><strong>/osf,</strong></a> que substitui a opção <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>modo inválido [alocar]</dt> <dd> Um modo inválido para a construção de atributo [<a href="allocate.md"><strong>ALLOCATE</strong></a>] foi especificado. Os quatro modos válidos são single_node, all_nodes, on_null e sempre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>atributos de comprimento não podem ser aplicados com atributo de cadeia de caracteres</dt> <dd> Quando o atributo de cadeia de caracteres é usado, os arquivos stub gerados chamam a função <strong>strlen</strong> para determinar o tamanho da cadeia de caracteres. Não use o atributo Length e o atributo String para a mesma variável.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[last_is] e [length_is] não podem ser especificados ao mesmo tempo</dt> <dd> Ambos [<a href="last-is.md"><strong>last_is</strong></a>] e [<a href="length-is.md"><strong>length_is</strong></a>] foram especificados para a mesma matriz. Esses atributos são relacionados da seguinte maneira: comprimento = último primeiro + 1. Como cada valor pode ser derivado do outro, não especifique ambos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[max_is] e [size_is] não podem ser especificados ao mesmo tempo</dt> <dd> Ambos [ <a href="max-is.md"><strong>max_is</strong></a>] e [ <a href="size-is.md"><strong>size_is</strong></a>] foram especificados para a mesma matriz. Esses atributos são relacionados da seguinte maneira: Max = size + 1. Como cada valor pode ser derivado do outro, não especifique ambos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>nenhum atributo [switch_is] especificado no uso de Union</dt> <dd> Nenhum discriminante foi especificado para a União. O atributo [<a href="switch-is.md"><strong>switch_is</strong></a>] indica o discriminante usado para selecionar entre os campos de União.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>nenhum [UUID] especificado</dt> <dd> Nenhum UUID foi especificado para a interface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[UUID] ignorado na interface [local]</dt> <dd> O uso do atributo [<a href="local.md"><strong>local</strong></a>] em uma interface de objeto faz com que o compilador MIDL ignore o atributo [<a href="uuid.md"><strong>UUID</strong></a>]. Você não pode usar ambos os atributos em uma interface RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>tipos incompatíveis entre expressões de atributo de comprimento e tamanho</dt> <dd> As expressões de atributo Length e Size devem ser dos mesmos tipos. Por exemplo, esse aviso é emitido quando a variável de atributo para a expressão [<a href="size-is.md"><strong>size_is</strong></a>] é do tipo <strong>não assinado</strong> e a variável de atributo para a expressão [<a href="length-is.md"><strong>length_is</strong></a>] é do tipo <a href="long.md"><strong>longo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>o atributo [String] deve ser um &quot; byte, &quot; &quot; Char &quot; ou &quot; wchar_t &quot; matriz ou ponteiro especificado</dt> <dd> Um atributo de cadeia de caracteres não pode ser aplicado a um ponteiro ou matriz cujo tipo base não seja um <a href="byte.md"><strong>byte</strong></a>, <a href="char-idl.md"><strong>Char</strong></a>ou <a href="struct.md"><strong>struct</strong></a> no qual os membros são todos os tipos de <strong>byte</strong> ou <strong>Char</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>incompatibilidade entre o tipo da expressão [switch_is] e o tipo de opção da União</dt> <dd> Se Union [<a href="switch-type.md"><strong>switch_type</strong></a>] não for especificado, o tipo de opção será o mesmo tipo do campo [<a href="switch-is.md"><strong>switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] não deve ser aplicado a um tipo que deriva de um identificador de contexto</dt> <dd> Identificadores de contexto não podem ser transmitidos como outros tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] deve especificar um tipo Transmissible</dt> <dd> O tipo [<a href="transmit-as.md"><strong>transmit_as</strong></a>] especificado deriva de um tipo que não pode ser transmitido pelo Microsoft RPC, como <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>ou <a href="int.md"><strong>int</strong></a>. Usar um tipo de base RPC definido; no caso de <strong>int</strong>, adicione especificadores de tamanho como <a href="small.md"><strong>pequeno</strong></a>, <a href="short.md"><strong>curto</strong></a>ou <a href="long.md"><strong>longo</strong></a> para qualificar o <strong>int</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>o tipo transmitido para [transmit_as] e [represent_as] não deve ser um ponteiro ou derivar de um ponteiro</dt> <dd> O tipo transmitido não pode ser um ponteiro ou derivar de um ponteiro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>o tipo apresentado para [transmit_as] e [represent_as] não deve derivar de uma matriz compatível/variável, seu equivalente de ponteiro ou uma estrutura compatível/variável</dt> <dd> O tipo ao qual [<a href="transmit-as.md"><strong>transmit_as</strong></a>] foi aplicado não pode derivar de uma matriz ou estrutura compatível (uma matriz ou estrutura cujo tamanho é determinado em tempo de execução).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>o formato [UUID] está incorreto</dt> <dd> O formato do UUID não está de acordo com a especificação. O UUID deve ser uma cadeia de caracteres que consiste em cinco sequências de dígitos hexadecimais de comprimento 8, 4, 4, 4 e 12 dígitos. &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; é um UUID válido. Use a função <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>UuidCreate</strong></a> ou um utilitário para gerar um UUID válido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>UUID não é um número hexadecimal</dt> <dd> O UUID especificado para a interface contém caracteres que são inválidos em uma representação de número hexadecimal. Os caracteres de 0 a 9 e A a F são válidos em uma representação hexadecimal.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>os parâmetros opcionais devem vir após os parâmetros obrigatórios</dt> <dd> Para obter uma descrição da ordenação de listas de parâmetros, consulte [<a href="optional.md"><strong>optional</strong></a>] na referência de linguagem MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[DllName] necessário quando [Entry] é usado</dt> <dd> Se você estiver especificando um ponto de entrada em uma DLL, também deverá especificar o nome dessa DLL usando o atributo [<a href="dllname-str-.md"><strong>DllName</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[vinculável] é inválido sem [propget], [propput] ou [propputref]</dt> <dd> O atributo [<a href="bindable.md"><strong>vinculável</strong></a>] é válido somente em uma propriedade, portanto, você também deve especificar uma das funções de acesso a propriedade ou de configuração de propriedade.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>os procedimentos com [propput] ou [propputref] devem ter pelo menos um parâmetro</dt> <dd> Um procedimento [<a href="propput.md"><strong>propput</strong></a>] ou [ <a href="propputref.md"><strong>propputref</strong></a>] deve ter pelo menos um parâmetro [<a href="in.md"><strong>in</strong></a>] com a propriedade a ser definida; um procedimento [<a href="propget.md"><strong>propget</strong></a>] deve ter pelo menos um parâmetro [<a href="out-idl.md"><strong>out</strong></a>, <a href="retval.md"><strong>retval</strong></a>] para receber a propriedade ou a referência.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>o atributo [ID] é necessário</dt> <dd> Essa função de membro, devido à sintaxe de <a href="dispinterface.md"><strong>dispinterface</strong></a> usada, requer um DISPID, que você especifica usando o atributo [ <a href="id.md"><strong>ID</strong></a>]. Quando você especifica um <strong>dispinterface</strong> usando propriedades e métodos, você deve especificar um DISPID para cada propriedade e método.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>o nome da interface especificado no ACF não corresponde ao especificado no arquivo IDL</dt> <dd> No modo de compilador atual, o nome que segue a palavra-chave da interface no ACF deve ser o mesmo que o nome que segue a palavra-chave da interface no arquivo IDL. Os nomes de interface nos arquivos IDL e ACF podem ser diferentes quando você compila com o <a href="-acf.md"><strong>/ACF</strong></a>do compilador MIDL switch.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>atributo duplicado</dt> <dd> Atributos duplicados ou conflitantes foram especificados. Esse erro geralmente ocorre quando dois atributos são mutuamente exclusivos. Por exemplo, os atributos [<a href="code.md"><strong>código</strong></a>] e [<a href="nocode.md"><strong>Nocode</strong></a>] não podem ser usados ao mesmo tempo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>o parâmetro com o atributo [comm_status] ou [fault_status] deve ser um ponteiro para o tipo error_status_t</dt> <dd> Quando [<a href="fault-status.md"><strong>fault_status</strong></a>] ou [<a href="comm-status.md"><strong>comm_status</strong></a>] é usado como um atributo de parâmetro, o parâmetro deve ser um parâmetro [<a href="out-idl.md"><strong>out</strong></a>] do tipo <a href="error-status-t.md"><strong>error_status_t</strong></a>. Se ocorrer um erro de servidor, o parâmetro será definido como o código de erro. Quando a chamada remota for concluída com êxito, o procedimento definirá o valor.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>um procedimento [local] não pode ser especificado no arquivo ACF</dt> <dd> Um procedimento local foi especificado no ACF. O procedimento local só pode ser especificado no arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>o tipo especificado não está definido como um identificador</dt> <dd> O tipo especificado no atributo [<a href="implicit-handle.md"><strong>implicit_handle</strong></a>] não está definido como um tipo de identificador. Altere a definição de tipo ou o nome de tipo especificado pelo atributo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>procedimento indefinido</dt> <dd> Um atributo foi aplicado a um procedimento no ACF e esse procedimento não está definido no arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>Este parâmetro não existe no arquivo IDL</dt> <dd> Um parâmetro especificado no ACF não existe na definição no arquivo IDL. Todos os parâmetros, funções e definições de tipo que aparecem no ACF devem corresponder a parâmetros, funções e tipos definidos anteriormente no arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>Não há suporte para esta construção de limites de matriz</dt> <dd> Atualmente, o MIDL dá suporte à expressa dos limites superior e inferior de uma matriz na matriz de formulário [inferior... Upper] somente quando a constante que especifica o limite inferior da matriz é resolvida para o valor zero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>especificação associada à matriz é inválida</dt> <dd> A especificação de usuário dos limites de matriz para a matriz de tamanho fixo é inválida. Por exemplo: <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>Ponteiro para uma matriz compatível ou uma matriz que contém uma matriz compatível não é suportada</dt> <dd> Uso de matriz compatível ilegal. Para regras que regem as matrizes em conformidade, consulte <a href="/windows/desktop/Rpc/arrays-and-rpc">matrizes e RPC</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>o ponto/matriz não deriva nenhum tamanho</dt> <dd> Uma matriz em conformidade foi especificada sem nenhuma especificação de tamanho. Você pode especificar o tamanho com o atributo [<a href="max-is.md"><strong>max_is</strong></a>] ou [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>somente matrizes fixas e SAFEARRAYs são válidos em uma biblioteca de tipos</dt> <dd> Você usou um tipo de matriz dentro de uma instrução de biblioteca que não pode ser usada em uma biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>SAFEARRAYs só são legais dentro de um bloco de biblioteca</dt> <dd> O compilador MIDL não reconhece um SAFEARRAY como um tipo de dados válido, exceto ao gerar uma biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>constante de caractere formada incorretamente</dt> <dd> O caractere de fim de linha não é permitido em constantes de caractere.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>fim do arquivo encontrado no comentário</dt> <dd> O caractere de fim de arquivo foi encontrado em um comentário.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>fim de arquivo encontrado na cadeia de caracteres</dt> <dd> O caractere de fim de arquivo foi encontrado em uma cadeia de caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>o comprimento do identificador excede 31 caracteres</dt> <dd> Os identificadores são limitados a 31 caracteres alfanuméricos. Nomes de identificadores com mais de 31 caracteres são truncados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>fim da linha encontrado na cadeia de caracteres</dt> <dd> O caractere de fim de linha foi encontrado na cadeia de caracteres. Verifique se você incluiu o caractere de aspas duplas que termina a cadeia de caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>a constante de cadeia de caracteres excede o limite de 255 caracteres</dt> <dd> A cadeia de caracteres excedeu o comprimento máximo permitido de 255 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>o identificador excede o limite de 255 caracteres e foi truncado</dt> <dd> O identificador excedeu o comprimento máximo permitido de 255 caracteres. Os caracteres em excesso no identificador são truncados.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>constante muito grande</dt> <dd> A constante é muito grande para ser representada internamente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>erro de análise numérica</dt> <dd> O compilador não pôde analisar o identificador numérico.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>erro ao abrir arquivo</dt> <dd> O sistema operacional relatou um erro ao tentar abrir um arquivo de saída. Esse erro pode ser causado por um nome muito longo para o sistema de arquivos ou por um nome de arquivo duplicado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>erro de associação à função<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>erro ao inicializar OLE<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>erro ao carregar biblioteca<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] somente o parâmetro não deve derivar de um ponteiro/matriz de nível superior [Unique] ou [PTR]</dt> <dd> Um ponteiro exclusivo não pode ser um parâmetro somente [<a href="out-idl.md"><strong>out</strong></a>]. Por definição, um ponteiro exclusivo pode mudar de <strong>nulo</strong> para não<strong>nulo</strong>. Nenhuma informação sobre o parâmetro somente [<strong>out</strong>] é passada do cliente para o servidor.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>o atributo não é aplicável a esta União não rpcable</dt> <dd> Somente os atributos [<a href="switch-is.md"><strong>switch_is</strong></a>] e [<a href="switch-type.md"><strong>switch_type</strong></a>] se aplicam a uma União que é transmitida como parte de uma chamada de procedimento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>a expressão usada para um atributo de tamanho não deve derivar de um parâmetro somente [out]</dt> <dd> O valor de um parâmetro somente [<a href="out-idl.md"><strong>out</strong></a>] não é transmitido para o servidor e não pode ser usado para determinar o comprimento ou o tamanho do parâmetro [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>a expressão usada para um atributo de comprimento para um parâmetro [in] não pode derivar de um parâmetro somente [out]</dt> <dd> O valor de um parâmetro somente [<a href="out-idl.md"><strong>out</strong></a>] não é transmitido para o servidor e não pode ser usado para determinar o comprimento ou o tamanho do parâmetro [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>uso de% de &quot; necessidades de int &quot; /c_ext</dt> <dd> MIDL é uma linguagem fortemente tipada. Todos os parâmetros transmitidos pela rede devem ser derivados de um dos tipos base de MIDL. O tipo <a href="int.md"><strong>int</strong></a> não é definido como parte de MIDL. Os dados transmitidos devem incluir um especificador de tamanho: <a href="small.md"><strong>pequeno</strong></a>, <strong>curto</strong>ou <strong>longo</strong>. Os dados que não são transmitidos pela rede podem ser incluídos em uma interface; Use a opção <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>o campo de struct/Union não deve ser &quot; void&quot;</dt> <dd> Os campos em uma estrutura ou União devem ser declarados como sendo de um tipo base específico com suporte de MIDL ou um tipo que é derivado dos tipos base. Tipos void não são permitidos em operações remotas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>o elemento da matriz não deve ser void</dt> <dd> Um elemento de matriz não pode ser void.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>uso de qualificadores de tipo e/ou de modificadores/ou c_ext</dt> <dd> Modificadores de tipo como <strong>_cdecl</strong> e <strong>_far</strong> podem ser compilados somente se você especificar a opção <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>o campo de struct/Union não deve derivar de uma função</dt> <dd> Os campos de uma estrutura ou União devem ser tipos base de MIDL ou tipos derivados desses tipos base. As funções não são legais em campos de estrutura ou União.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>o elemento da matriz não deve ser uma função</dt> <dd> Um elemento de matriz não pode ser uma função.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>o parâmetro não deve ser uma função</dt> <dd> O parâmetro para um procedimento remoto deve ser uma variável de um tipo especificado. Uma função não pode ser um parâmetro para o procedimento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>struct/Union com campos de bits necessários/c_ext</dt> <dd> Você deve especificar a opção <a href="-c-ext.md"><strong>/c_ext</strong></a> do compilador MIDL para permitir campos de bits em estruturas que não são transmitidas em uma chamada de procedimento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>especificação de campo de bits em um tipo diferente de &quot; int &quot; é uma extensão não compatível com ANSI</dt> <dd> A especificação da linguagem de programação ANSI C não permite que os campos de bits sejam aplicados a tipos não inteiros.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>a especificação de campo de bits pode ser aplicada somente a tipos simples e integrais</dt> <dd> A especificação da linguagem de programação ANSI C não permite que os campos de bits sejam aplicados a tipos não inteiros.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>o campo de struct/Union não deve derivar de handle_t ou de um manipulador de contexto</dt> <dd> Identificadores de contexto não podem ser transmitidos como parte de outra estrutura. Eles devem ser transmitidos como identificadores de contexto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>o elemento de matriz não deve derivar de handle_t ou um identificador de contexto</dt> <dd> Identificadores de contexto não podem ser transmitidos como parte de uma matriz.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>Esta especificação de Union precisa/c_ext</dt> <dd> Uma União que aparece na definição de interface deve ser associada ao discriminante ou declarada como local. Os dados que não são transmitidos pela rede podem ser declarados implicitamente como locais quando você usa a opção <a href="-c-ext.md"><strong>/c_ext</strong></a> , que é o padrão MIDL. Não é possível compilar essa IDL com a opção <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>o parâmetro derivado de um &quot; int &quot; deve ter um especificador de tamanho &quot; pequeno, &quot; &quot; curto &quot; ou &quot; longo &quot; com o &quot; int&quot;</dt> <dd> O tipo <a href="int.md"><strong>int</strong></a> é apenas um tipo de MIDL válido em plataformas de 32 bits, em sistemas de 16 bits <strong>int</strong> deve ser acompanhado de uma especificação de tamanho. Use um dos especificadores de tamanho <a href="small.md"><strong>pequeno</strong></a>, <a href="short.md"><strong>curto</strong></a>ou <a href="long.md"><strong>longo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>o tipo do parâmetro não pode derivar de void ou void *</dt> <dd> MIDL é uma linguagem fortemente tipada. Todos os parâmetros transmitidos pela rede devem ser derivados de um dos tipos base de MIDL. MIDL não dá suporte a <a href="void.md"><strong>void</strong></a> como tipo base. Você deve alterar a declaração para um tipo de MIDL válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>Não há suporte para o parâmetro derivado de uma struct/Union contendo campos de bits</dt> <dd> Os campos de bits não são definidos como um tipo de dados válido pelo RPC DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>uso de um parâmetro derivado de um tipo que contém o tipo-modificadores/tipo-qualificadores precisa/c_ext</dt> <dd> O uso de palavras-chave, como a <strong>distância</strong>, <strong>Near</strong>, <a href="const.md"><strong>const</strong></a>e <strong>volatile</strong> no arquivo IDL, é uma extensão da Microsoft para a DCE do DTE. Essas palavras-chave não estão disponíveis quando você compila com o comutador <a href="-osf.md"><strong>/OSF</strong></a> , que desativa a opção de extensão padrão <a href="-c-ext.md"><strong>/c_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>o parâmetro não deve derivar de um ponteiro para uma função</dt> <dd> As bibliotecas de tempo de execução RPC transmitem um ponteiro e seus dados associados entre o cliente e o servidor. Ponteiros para funções não podem ser transmitidos como parâmetros porque a função não pode ser transmitida pela rede.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>o parâmetro não deve derivar de uma União compatível com nonrpc</dt> <dd> A União deve ser associada a um discriminante. Use os atributos [<a href="switch-is.md"><strong>switch_is</strong></a>] e [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>o tipo de retorno deriva de um &quot; int. &quot; Você deve usar especificadores de tamanho com o &quot; int&quot;</dt> <dd> Em sistemas de 16 bits, o tipo <a href="int.md"><strong>int</strong></a> não é um tipo MIDL válido, a menos que seja acompanhado por uma especificação de tamanho. Use um dos especificadores de tamanho <a href="small.md"><strong>pequeno</strong></a>, <a href="short.md"><strong>curto</strong></a>ou <a href="long.md"><strong>longo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>o tipo de retorno não deve derivar de um ponteiro void</dt> <dd> MIDL é uma linguagem fortemente tipada. Todos os parâmetros transmitidos pela rede devem ser derivados de um dos tipos base de MIDL. Tipos void não são definidos como parte de MIDL. Você deve alterar a declaração para um tipo de MIDL válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>o tipo de retorno não deve derivar de uma estrutura/União que contém campos de bits</dt> <dd> Os campos de bits não são definidos como um tipo de dados válido pelo RPC DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>o tipo de retorno não deve derivar de uma União compatível com nonrpc</dt> <dd> A União deve ser associada a um discriminante. Use os atributos [<a href="switch-is.md"><strong>switch_is</strong></a>] e [<a href="switch-type.md"><strong>switch_type</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>o tipo de retorno não deve derivar de um ponteiro para uma função</dt> <dd> As bibliotecas de tempo de execução RPC transmitem um ponteiro e seus dados associados entre o cliente e o servidor. Ponteiros para funções não podem ser transmitidos como parâmetros porque RPC não define um método para transmitir a função associada pela rede.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>Não há suporte para inicializadores compostos</dt> <dd> O RPC da DCE dá suporte apenas à inicialização simples. A estrutura ou a matriz não pode ser inicializada no arquivo IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>Os atributos de ACF no arquivo IDL precisam da opção/app_config</dt> <dd> Uma extensão da Microsoft permite que você especifique atributos de ACF no arquivo IDL. Use a opção <a href="-app-config.md"><strong>/app_config</strong></a> para ativar essa extensão.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>o comentário de linha única precisa/ms_ext ou/c_ext</dt> <dd> Comentários de linha única que usam dois caracteres de barra (//) representam uma extensão da Microsoft para o RPC da DCE. Você não poderá usar comentários de linha única se estiver Compilando com a opção <a href="-osf.md"><strong>/OSF</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>o formato de [Version] está incorreto</dt> <dd> O número de versão da interface no cabeçalho da interface deve ser especificado no formato <em>principal</em>. <em>secundária</em>, onde cada número pode variar de 0 a 65535.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;&quot;requisitos/ms_ext ou/c_ext assinados</dt> <dd> O uso da palavra-chave <a href="signed.md"><strong>assinada</strong></a> é uma extensão da Microsoft para o DCE do DTE. Você não poderá usar a opção <a href="-osf.md"><strong>/OSF</strong></a> se quiser usar esse recurso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>incompatibilidade no tipo de atribuição</dt> <dd> O tipo da variável não corresponde ao tipo do valor que é atribuído à variável.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>a declaração deve estar no formato: &lt; tipo const&gt;<declarator> = <initializing expression></dt> <dd> A declaração não é compatível com a sintaxe de RPC da DCE. Use a <a href="-ms-ext.md"><strong>opção /ms_ext</strong></a> <a href="-c-ext.md"><strong>ou /c_ext</strong></a> do compilador MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>a declaração deve ter &quot; const&quot;</dt> <dd> As declarações no arquivo IDL devem ser expressões constantes que usam a palavra-chave <a href="const.md"><strong>const</strong></a>, por exemplo:<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>struct/union/enum não deve ser definido em uma especificação de tipo de parâmetro</dt> <dd> A estrutura, a união ou o tipo enumerado devem ser explicitamente declarados fora do protótipo de função.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>O atributo [allocate] deve ser aplicado somente em tipos de ponteiro não nulos</dt> <dd> O atributo [<a href="allocate.md"><strong>allocate</strong></a>] foi projetado para estruturas de dados complexas baseadas em ponteiro. Quando o atributo [allocate] é especificado, o arquivo stub atravessa a estrutura de dados para calcular o tamanho total de todos os objetos acessíveis do ponteiro e todos os outros ponteiros na estrutura de dados. Altere o tipo para um tipo de ponteiro nãovoid ou remova o atributo [<strong>allocate</strong>] e use outro método para determinar seu tamanho de alocação, como <strong>o operador sizeof.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>matriz ou constructo de ponteiro equivalente não pode derivar de uma união não truncada</dt> <dd> Cada união deve ser associada a um discriminante. Matrizes de uniões não são permitidas porque não fornecem o discriminante associado. Matrizes de estruturas nas quais a estrutura em pacotes a união e seu discriminante são permitidas porque os stubs podem usar o discriminante para determinar o tamanho de cada união.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>field não deve derivar de um error_status_t tipo</dt> <dd> O <a href="error-status-t.md"><strong>error_status_t</strong></a> tipo somente pode ser usado como um parâmetro ou um tipo de retorno. Ele não pode ser inserido no campo de uma estrutura ou união.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>union tem pelo menos um arm sem um rótulo de caso</dt> <dd> A declaração de união não é correspondente à sintaxe MIDL necessária para a união. Cada arm de união requer um rótulo de caso ou rótulo padrão que seleciona esse arm de união.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>parâmetro ou valor de retorno não deve derivar de um tipo que tem [ignorar] aplicado a ele</dt> <dd> O atributo [<a href="ignore.md"><strong>ignore</strong></a>] é um atributo de campo que pode ser aplicado somente a campos, como campos de estruturas e matrizes. O atributo [<strong>ignore</strong>] indica que o stub não deve desreferenciar o ponteiro durante a transmissão e não é permitido quando entra em conflito com outros atributos que devem ser desreferenciados, como parâmetros [<a href="out-idl.md"><strong>out</strong></a>] e valores de retorno de função.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>o ponteiro já tem um atributo de ponteiro aplicado a ele</dt> <dd> Somente um dos atributos de ponteiro, [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>unique</strong></a>], ou [<a href="ptr.md"><strong>ptr</strong></a>], pode ser aplicado a um único ponteiro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>field/parameter não deve derivar de uma estrutura recursiva por meio de um ponteiro ref</dt> <dd> Por definição, um ponteiro de referência não pode ser definido como <strong>NULL.</strong> Uma estrutura de dados recursiva definida com um ponteiro de referência não tem <strong>elementos NULL</strong> e, por convenção, não é finalizada. Use um atributo de ponteiro [<a href="unique.md"><strong>exclusivo</strong></a>] para permitir que a estrutura de dados especifique um elemento <strong>NULL</strong> ou redefina a estrutura de dados como uma estrutura de dados não recursiva.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>O uso do campo que deriva de um ponteiro nulo precisa de /c_ext</dt> <dd> O tipo <strong>void *</strong> e outros tipos e qualificadores de tipo que não são suportados pela IDL de DCE só são permitidos no arquivo IDL quando você usa as configurações do compilador padrão MIDL. Usar a <a href="-osf.md"><strong>opção /osf</strong></a> substitui esse padrão. Se você precisar compilar no modo osf-compatibility, precisará redefinir o tipo de ponteiro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>O uso desse atributo precisa de /ms_ext</dt> <dd> Esse recurso de linguagem é uma extensão da Microsoft para ADL de DCE. Você não poderá usar esse recurso se estiver compilando no modo de compatibilidade de osf ( <a href="-osf.md"><strong>/osf</strong></a> ).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>esse atributo só é permitido com novas bibliotecas de tipos de formato</dt> <dd> Para usar esse atributo, você precisa da versão do Oleaut32.dll fornecida com Windows 2000 ou posterior.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>uso de wchar_t precisa de /ms_ext ou /c_ext</dt> <dd> O tipo de caractere largo representa uma extensão para ADL de DCE. O compilador MIDL não aceita o tipo de caractere largo quando você especifica a <a href="-osf.md"><strong>opção /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>os campos sem nome precisam de /ms_ext ou /c_ext</dt> <dd> A IDL de DCE não dá suporte ao uso de estruturas ou uniões sem nome inseridas em outras estruturas ou uniões. Na IDL do DCE, todos esses campos inseridos devem ser nomeados. O compilador MIDL não permite seu uso quando você especifica a <a href="-osf.md"><strong>opção /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>campos sem nome só podem derivar de tipos struct/union</dt> <dd> A extensão da Microsoft para a IDL de DCE que dá suporte a campos sem nome se aplica somente a estruturas e uniões. Você deve atribuir um nome ao campo ou redefinir o campo para cumprir essa restrição.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>O campo de uma união não pode derivar de uma matriz compatível/variável ou de seu ponteiro equivalente</dt> <dd> A matriz compatível não pode aparecer sozinha na união, mas deve ser acompanhada pelo valor que especifica o tamanho da matriz. Em vez de usar a matriz como o arm de união, use uma estrutura que consiste na matriz compatível e no identificador que especifica seu tamanho.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>nenhum atributo [pointer_default] especificado, supondo que [ptr] para todos os ponteiros não atribuídos na interface</dt> <dd> A implementação de IDL de DCE especifica que todos os ponteiros em cada arquivo IDL devem ser associados a atributos de ponteiro. Quando um atributo de ponteiro explícito não é atribuído ao tipo de parâmetro ou ponteiro e nenhum atributo [<a href="pointer-default.md"><strong>pointer_default</strong></a>] é especificado no arquivo IDL, o atributo de ponteiro completo <a href="ptr.md"><strong>ptr</strong></a> é associado ao ponteiro. Você pode alterar os atributos de ponteiro usando atributos de ponteiro explícitos, especificando um atributo [<strong>pointer_default</strong>] ou especificando a opção <a href="-ms-ext.md"><strong>/ms_ext</strong></a> para alterar o padrão para ponteiros não atribuídos para [<a href="unique.md"><strong>exclusivo</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>A expressão de inicialização deve ser resolvida para uma expressão constante</dt> <dd> Se uma expressão for usada como um inicializador, a expressão deverá ser uma expressão constante. Isso é verdadeiro em todos os modos do compilador MIDL. A expressão deve ser resolvível no tempo de compilação. Especifique uma constante literal ou uma expressão que seja resolvida para uma constante, em vez de uma variável.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>A expressão de atributo deve ser do tipo integer, char, Boolean ou enum</dt> <dd> O tipo especificado não é resolvido para um tipo de opção válido. Use um tipo inteiro, caractere, <a href="byte.md"><strong>byte</strong></a>, <a href="boolean.md"><strong>booliana</strong></a>ou <a href="enum.md"><strong>enum</strong></a> ou um tipo derivado de um desses tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>constante ilegal</dt> <dd> A constante especificada está fora do intervalo válido para o tipo especificado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>atributo não implementado; Ignorado</dt> <dd> O atributo especificado não é implementado nesta versão do Microsoft RPC. O compilador MIDL continua processando o arquivo IDL como se o atributo não estivesse presente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>O tipo de retorno não deve derivar de um ponteiro [ref]</dt> <dd> Os valores de retorno de função definidos como tipos de ponteiro devem ser especificados como [<a href="unique.md"><strong>exclusivo</strong></a>] ou <a href="ptr.md"><strong>ponteiros</strong></a> completos. Não é possível usar ponteiros de referência.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>A expressão de atributo deve ser um nome de variável ou uma expressão de desreferência de ponteiro nesse modo. Você deve especificar a opção /ms_ext</dt> <dd> O compilador IDL de DCE requer que o tamanho associado ao atributo [<a href="size-is.md"><strong>size_is</strong></a>] seja especificado por uma variável ou variável de ponteiro. Se você quiser aproveitar a extensão da Microsoft que permite que o atributo [<strong>size_is</strong>] seja definido por uma expressão constante, não poderá usar a opção do compilador <a href="-osf.md"><strong>/osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>O parâmetro não deve derivar de uma união não truncada recursiva</dt> <dd> Uma união deve incluir um discriminante, portanto, uma união não pode ter outra união como um elemento. Uma união pode ser inserida em outra união somente quando faz parte de uma estrutura que inclui o discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>o parâmetro de identificador de associação não pode ser [fora] somente</dt> <dd> O parâmetro de identificador identificado pelo compilador MIDL como o identificador de associação para esta operação deve ser um parâmetro [<a href="in.md"><strong>in</strong></a>]. [<a href="out-idl.md"><strong>out</strong></a>]-os parâmetros somente são indefinidos no stub do cliente e o identificador de associação deve ser definido no cliente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>o ponteiro para um identificador não pode ser [Unique] ou [PTR]</dt> <dd> Você não pode usar os atributos de ponteiro exclusivo e completo para um ponteiro para um identificador. Esses atributos permitem o valor <strong>NULL</strong>e o identificador de associação não pode ser <strong>nulo</strong>. Use o atributo [<a href="ref.md"><strong>ref</strong></a>] para derivar o parâmetro de identificador de associação de ponteiros de referência.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>o parâmetro que não é um identificador de associação não deve derivar de handle_t</dt> <dd> O tipo de identificador primitivo <a href="handle-t.md"><strong>handle_t</strong></a> não é um tipo de dados válido que é transmitido pela rede. Altere o tipo de parâmetro para um tipo diferente de <strong>handle_t</strong>ou remova o parâmetro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>fim de arquivo inesperado encontrado</dt> <dd> O compilador MIDL encontrou o final do arquivo antes de poder resolver com êxito todos os elementos sintáticas do arquivo. Verifique se o caractere de término da chave direita (}) está presente no final do arquivo ou verifique a sintaxe.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>o tipo derivado de handle_t não deve ter [transmit_as] aplicado a ele</dt> <dd> O tipo de identificador primitivo <a href="handle-t.md"><strong>handle_t</strong></a> não é transmitido pela rede.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] não deve ser aplicado a um tipo que tem [Handle] aplicado a ele</dt> <dd> Os atributos [<a href="context-handle.md"><strong>context_handle</strong></a>] e [<a href="handle.md"><strong>Handle</strong></a>] não podem ser aplicados ao mesmo tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[Handle] não deve ser especificado em um tipo derivado de void ou void *</dt> <dd> Um tipo especificado com o atributo [<a href="handle.md"><strong>Handle</strong></a>] pode ser transmitido pela rede, mas o tipo <strong>void *</strong> não é um tipo Transmissible. O tipo de identificador deve ser resolvido para um tipo que deriva dos tipos base Transmissible.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>o parâmetro deve ter [in], [out] ou [in, out] nesse modo. Você deve especificar/ms_ext ou/c_ext</dt> <dd> O compilador de IDL do DCE requer que todos os parâmetros tenham parâmetros direcionais explícitos. Para usar as extensões da Microsoft para IDL do DCE, você não pode usar a opção <a href="-osf.md"><strong>/OSF</strong></a> , que substitui <a href="-ms-ext.md"><strong>/ms_ext</strong></a> e <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>o tipo transmitido não pode derivar de &quot; void &quot; para [transmit_as], [represent_as], [wire_marshal], [user_marshal]</dt> <dd> O atributo [<a href="transmit-as.md"><strong>transmit_as</strong></a>] aplica-se somente a tipos de ponteiro. Use o tipo <strong>void *</strong> no lugar de <a href="void.md"><strong>void</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;void &quot; deve ser especificado na primeira e única especificação de parâmetro</dt> <dd> A palavra-chave <a href="void.md"><strong>void</strong></a> aparece incorretamente com outros parâmetros de função. Para especificar uma função sem parâmetros, a palavra-chave <strong>void</strong> deve ser o único elemento da lista de parâmetros, como no exemplo a seguir:<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[switch_is] deve ser especificado somente em um tipo derivado de uma União não encapsulada</dt> <dd> A palavra-chave [<a href="switch-is.md"><strong>switch_is</strong></a>] foi aplicada incorretamente. Ele só pode ser usado com <a href="nonencapsulated-unions.md">tipos de União não encapsulados</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>estruturas de cadeia de caracteres não são implementadas nesta versão</dt> <dd> O DCE IDL permite que o atributo [<a href="string.md"><strong>String</strong></a>] se aplique a uma estrutura cujos elementos consistem apenas em caracteres, bytes ou tipos que são resolvidos para caracteres ou bytes. Não há suporte para essa funcionalidade no Microsoft RPC. O atributo [<strong>String</strong>] não pode ser aplicado à estrutura como um todo. No entanto, ele pode ser aplicado a cada matriz individual.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>o tipo de comutador só pode ser integral, Char, Boolean ou enum</dt> <dd> O tipo especificado não é resolvido para um tipo de opção válido. Use um inteiro, caractere, <a href="byte.md"><strong>byte</strong></a>, <a href="boolean.md"><strong>booliano</strong></a>, tipo de <a href="enum.md"><strong>Enumeração</strong></a> ou um tipo derivado de um desses tipos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[Handle] não deve ser especificado em um tipo derivado de handle_t</dt> <dd> Um tipo de identificador deve ser definido usando um e apenas um dos tipos de identificadores ou atributos. Use o tipo primitivo <a href="handle-t.md"><strong>handle_t</strong></a> ou o atributo [<a href="handle.md"><strong>Handle</strong></a>], mas não ambos. O tipo de identificador definido pelo usuário deve ser transmissible, mas o tipo de <strong>handle_t</strong> não é transmitido na rede.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>o parâmetro derivado de handle_t não deve ser um parâmetro [out]</dt> <dd> Um identificador do tipo primitivo <a href="handle-t.md"><strong>handle_t</strong></a> é significativo apenas para o lado do aplicativo no qual ele está definido. O tipo <strong>handle_t</strong> não é transmitido na rede.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>a expressão de atributo deriva de uma referência de ponteiro [Unique] ou [PTR]</dt> <dd> Embora os atributos de ponteiro <a href="ptr.md"><strong>completo</strong></a> [<a href="unique.md"><strong>Unique</strong></a>] e Full permitam que os ponteiros tenham valores <strong>nulos</strong> , a expressão que define o tamanho ou o atributo de comprimento nunca deve ter um valor <strong>nulo</strong> . Quando ponteiros são usados, MIDL restringe expressões a ponteiros [<a href="ref.md"><strong>ref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; requer/ms_ext</dt> <dd> O atributo <a href="cpp-quote.md"><strong>cpp_quote</strong></a> é uma extensão da Microsoft para o DCE IDL. Não use a opção de compilador MIDL <a href="-osf.md"><strong>/OSF</strong></a>, que substitui <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>UUID entre aspas requer/ms_ext</dt> <dd> A capacidade de especificar um valor de UUID entre aspas é uma extensão da Microsoft para o DCE IDL. Não use a opção de compilador MIDL <a href="-osf.md"><strong>/OSF</strong></a>, que substitui <a href="-ms-ext.md"><strong>/ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>tipo de retorno não pode derivar de uma União não encapsulada</dt> <dd> A União não encapsulada não pode ser usada como um tipo de retorno de função. Para retornar o tipo de União, especifique o tipo de União como um parâmetro [<a href="out-idl.md"><strong>out</strong></a>] ou [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>tipo de retorno não pode derivar de uma estrutura compatível</dt> <dd> O tamanho do tipo de retorno deve ser uma constante. Não é possível especificar como um tipo de retorno uma estrutura que contém uma matriz em conformidade mesmo quando a estrutura também inclui seu especificador de tamanho. Para retornar a estrutura compatível, especifique a estrutura como um parâmetro [<a href="out-idl.md"><strong>out</strong></a>] ou [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] não deve ser aplicado a um tipo derivado de um identificador genérico</dt> <dd> Nesta versão, os atributos [<a href="handle.md"><strong>Handle</strong></a>] e [<a href="transmit-as.md"><strong>transmit_as</strong></a>] não podem ser combinados no mesmo tipo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[Handle] não deve ser aplicado a um tipo que tem [transmit_as] aplicado a ele</dt> <dd> Nesta versão, os atributos [<a href="handle.md"><strong>Handle</strong></a>] e [<a href="transmit-as.md"><strong>transmit_as</strong></a>] não podem ser combinados no mesmo tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>o tipo especificado para a declaração Const é inválido</dt> <dd> Declarações de constantes são limitadas a tipos inteiros, caracteres, caracteres largos, cadeias de caracteres e boolianos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>Não há suporte para o operando para o operador sizeof</dt> <dd> O compilador MIDL dá suporte à operação <strong>sizeof</strong> apenas para tipos simples. O operando especificado não é avaliado como um tipo inteiro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>Este nome já foi usado como um nome de identificador const</dt> <dd> O identificador foi usado anteriormente para identificar uma constante em uma declaração <a href="const.md"><strong>const</strong></a> . Altere o nome de um dos identificadores para que os identificadores sejam exclusivos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>redefinição inconsistente do tipo error_status_t</dt> <dd> O tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> deve resolver para o tipo <strong>unsigned long.</strong> Outras definições de tipo não podem ser usadas.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[case] valor fora do intervalo do tipo de opção</dt> <dd> O valor associado ao caso da instrução switch está fora do intervalo para o tipo de opção especificado. Por exemplo, esse erro ocorre quando um valor inteiro longo é usado na instrução case para um tipo inteiro curto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>parâmetro que deriva de wchar_t /ms_ext</dt> <dd> O tipo de caractere largo <a href="wchar-t.md"><strong>wchar_t</strong></a> é uma extensão da Microsoft para ADL de DCE. Não use a opção <a href="-osf.md"><strong>/osf do</strong></a>compilador MIDL, que substitui <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>essa interface tem apenas retornos de chamada</dt> <dd> Os retornos de chamada são válidos somente no contexto de uma chamada de procedimento remoto. A interface deve incluir pelo menos um protótipo de função para uma chamada de procedimento remoto que não inclui o atributo [<a href="callback.md"><strong>retorno de chamada</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>atributo especificado com redundância; Ignorado</dt> <dd> O atributo especificado foi aplicado mais de uma vez. Várias instâncias do mesmo atributo são ignoradas.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>tipo de identificador de contexto usado para um identificador implícito</dt> <dd> Um tipo que foi definido usando o atributo [<a href="context-handle.md"><strong>context_handle</strong></a>] foi especificado como o tipo de identificador em um atributo [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>] . Os atributos não podem ser combinados dessa maneira.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>opções conflitantes especificadas para [alocar]</dt> <dd> As opções especificadas para o atributo ACF [<a href="allocate.md"><strong>allocate</strong></a>] representam diretivas conflitantes. Por exemplo, especifique a opção all_nodes ou a opção single_node, mas não ambas.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>erro ao escrever no arquivo</dt> <dd> Ocorreu um erro ao escrever no arquivo. Essa condição pode ser causada por erros relacionados a espaço em disco, alças de arquivo, restrições de acesso a arquivos e falhas de hardware.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>nenhum tipo de opção encontrado na definição de união, usando o tipo [switch_is]</dt> <dd> A definição de união não inclui um atributo [<a href="switch-type.md"><strong>switch_type</strong></a>] explícito. O tipo da variável especificada pelo atributo [<a href="switch-is.md"><strong>switch_is</strong></a>] é usado como o tipo de opção.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>verificação semântica incompleta devido a erros anteriores</dt> <dd> O compilador MIDL faz duas passagens sobre os arquivos de entrada para resolver as declarações de encaminhamento. Devido a erros encontrados durante a primeira passagem, a verificação da segunda passagem não foi executada. Erros não relatados relacionados a declarações de encaminhamento ainda podem estar presentes no arquivo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>não há suporte para o parâmetro handle ou o tipo de retorno em um procedimento [retorno de chamada]</dt> <dd> Um procedimento [<a href="callback.md"><strong>retorno</strong></a>de chamada ] ocorre no contexto de uma chamada de um cliente para o servidor e usa o mesmo alça de associação que a chamada original. Parâmetros explícitos de alça de associação ou tipos de retorno não são permitidos em funções de retorno de chamada.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[ptr] não dá suporte ao alias nesta versão</dt> <dd> Um alias ocorre quando os dados são acessíveis por meio de mais de um ponteiro ou nome de variável. Remova o alias. Para obter mais informações, consulte <a href="/windows/desktop/Rpc/unique-pointers">Ponteiros exclusivos.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>parâmetro já definido como um alça de contexto</dt> <dd> O parâmetro foi definido anteriormente como um alça de contexto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] não deve derivar de handle_t</dt> <dd> As três características de identificador: o <a href="handle-t.md"><strong>tipo handle_t</strong></a>, o atributo [<a href="handle.md"><strong>handle</strong></a>], e o atributo [<a href="context-handle.md"><strong>context_handle</strong></a>], são mutuamente exclusivos. Apenas uma característica pode ser aplicada a um tipo ou parâmetro por vez.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>O tamanho da matriz excede 65536 bytes</dt> <dd> Em algumas plataformas da Microsoft, o tamanho máximo de dados permitidos é de 64K. Reprojete seu aplicativo para que todos os dados transmitidos se ajustem ao tamanho máximo permitido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>O tamanho da estrutura excede 65536 bytes</dt> <dd> Em algumas plataformas da Microsoft, o tamanho máximo de dados permitidos é de 64K. Reprojete seu aplicativo para que todos os dados transmitidos se ajustem ao tamanho máximo permitido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>O campo de uma união não truncada não pode ser outra união não truncada</dt> <dd> Uniões transmitidas como parte de uma chamada de procedimento remoto exigem um item de dados associado, o discriminante, que seleciona o arm de união. Uniões aninhadas em outras uniões não oferecem um discriminante; como resultado, eles não podem ser transmitidos neste formulário. Crie uma estrutura que consiste na união e em seu discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>atributos de ponteiro aplicados em uma matriz inserida; Ignorado</dt> <dd> Um atributo de ponteiro pode ser aplicado a uma matriz somente quando a matriz é um parâmetro de nível superior. Outros atributos de ponteiro aplicados a matrizes inseridas em outras estruturas de dados são ignorados.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[allocate] é ilegal no tipo transmitido ou apresentado para [transmit_as], [represent_as], [wire_marshal] ou [user_marshal]</dt> <dd> Os atributos [<a href="transmit-as.md"><strong>transmit_as</strong></a>] e [<a href="allocate.md"><strong>allocate</strong></a>] não podem ser aplicados ao mesmo tipo. O atributo [<strong>transmit_as</strong>] distingue entre os tipos apresentados e transmitidos, enquanto o atributo [<strong>allocate</strong>] pressuém que o tipo apresentado é o mesmo que o tipo transmitido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>[switch_type] deve ser especificado neste modo de importação<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] tipo indefinido; supondo que o handle genérico</dt> <dd> O tipo de identificador especificado no ACF não está definido no arquivo IDL. O compilador MIDL assume que o tipo de identificador é resolvido para o tipo de identificador <a href="handle-t.md"><strong>primitivo handle_t</strong></a>. Adicione o atributo [<a href="handle.md"><strong>handle</strong></a>] à definição de tipo se você quiser que o identificador se comporte como um identificador genérico ou definido pelo usuário.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>O elemento array não deve derivar de error_status_t</dt> <dd> Nesta versão do Microsoft RPC, o tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> pode aparecer apenas como um parâmetro ou tipo de retorno. Ele não pode aparecer em matrizes.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[alocar] ilegal em um tipo que deriva de um identificador primitivo/genérico/de contexto</dt> <dd> Por design, o atributo ACF [<a href="allocate.md"><strong>allocate</strong></a>] não pode ser aplicado a tipos de alça.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>O tipo transmitido ou apresentado não deve derivar de error_status_t</dt> <dd> Nesta versão do Microsoft RPC, o tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> não pode ser usado com o atributo [<a href="transmit-as.md"><strong>transmit_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>discriminante de uma união não deve derivar de um campo com [ignorar] aplicado a ela</dt> <dd> Uma união usada em uma chamada de procedimento remoto deve ser associada a outro item de dados, chamado discriminante, que seleciona o arm de união. O discriminante deve ser transmitido. O atributo [<a href="ignore.md"><strong>ignore</strong></a>] não pode ser aplicado ao discriminante de união.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[Nocode] ignorado para o lado do servidor, pois o &quot; /Server None &quot; não foi especificado</dt> <dd> Alguns compiladores de IDL do DCE geram um erro quando o atributo [<a href="nocode.md"><strong>Nocode</strong></a>] é aplicado a um procedimento em uma interface para a qual os arquivos stub de servidor estão sendo gerados. Como o servidor deve dar suporte a todas as operações, [<strong>Nocode</strong>] não deve ser aplicado a um procedimento nesse modo, ou você deve usar a opção de compilador MIDL <a href="-server.md"><strong>/Server</strong></a> None para especificar explicitamente que nenhuma rotina de servidor seja gerada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>nenhum procedimento remoto especificado na interface não [local]; nenhum stub de cliente/servidor será gerado</dt> <dd> A interface fornecida não tem nenhum procedimento remoto, portanto, somente os arquivos de cabeçalho serão gerados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>muitos casos padrão especificados para União encapsulada</dt> <dd> Uma União encapsulada pode ter apenas um padrão: ARM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>muitas interfaces padrão especificadas para coclass</dt> <dd> Uma <a href="coclass.md"><strong>coclass</strong></a> pode ter no máximo dois membros [<a href="default.md"><strong>Default</strong></a>], um para representar a interface de saída (origem) ou dispinterface e outro para representar a interface de entrada (coletor) ou Dispinterface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>os itens com [defaultvtable] também devem ter [Source]</dt> <dd> A interface <a href="defaultvtable.md"><strong>defaultvtable</strong></a> cria uma segunda interface de origem para um objeto, que permite que os coletores recebam eventos por meio da tabela V.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>a especificação Union sem campos é ilegal</dt> <dd> As uniões devem ter pelo menos um campo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>valor fora do intervalo</dt> <dd> O valor de case fornecido está fora do intervalo do tipo de comutador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] deve ser aplicado em um tipo de ponteiro</dt> <dd> Os identificadores de contexto sempre devem ser tipos de ponteiro. A DCE especifica que todos os identificadores de contexto devem ser digitados como <strong>void *</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>o tipo de retorno não deve derivar de handle_t</dt> <dd>Não é possível retornar <a href="handle-t.md"><strong>handle_t</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[Handle] não deve ser aplicado a um tipo derivado de um identificador de contexto</dt> <dd> Um tipo não pode ser um identificador de contexto e um identificador genérico.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>o campo derivado de um &quot; int &quot; deve ter um especificador de tamanho &quot; pequeno &quot; , &quot; curto &quot; ou &quot; longo &quot; com o &quot; int&quot;</dt> <dd> O tipo <a href="int.md"><strong>int</strong></a> não é Transmissible em sistemas de 16 bits, já que o tamanho de <strong>int</strong> pode ser diferente entre os computadores.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>o campo não deve derivar de um void ou void *</dt> <dd> <strong>void</strong> e <strong>void *</strong> não podem ser usados como tipos de parâmetro para procedimentos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>o campo não deve derivar de uma estrutura que contém campos de bits</dt> <dd> Estruturas contendo campos de bits não podem ser usadas como parâmetros ou tipos de retorno para procedimentos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>o campo não deve derivar de uma União não rpcable</dt> <dd> Uma Union deve ser especificada como uma União não encapsulada ou uma União encapsulada para ser transmitida. As uniões comuns de C não têm o discriminante necessário para transmitir a União pela rede.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>o campo não deve derivar de um ponteiro para uma função</dt> <dd> Ponteiros para funções não podem ser transmitidos para procedimentos remotos. Ponteiros para funções apontam para o código de função e nenhum código de função pode ser transmitido pela rede usando RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>Não é possível usar [fault_status] em um parâmetro e um tipo de retorno</dt> <dd> O atributo [<a href="fault-status.md"><strong>fault_status</strong></a>] pode ser usado apenas uma vez por procedimento. O atributo [<a href="comm-status.md"><strong>comm_status</strong></a>] pode ser usado de forma independente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>tipo de retorno muito complicado para modos/Oi, usando/os</dt> <dd> Tipos de retorno grandes que são passados pelo valor só podem ser tratados por stubs de otimização <a href="-os.md"><strong>/os</strong></a> . Os stubs para essa rotina serão gerados usando a otimização de <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>tipo de identificador genérico muito grande para modos/Oi, usando/os</dt> <dd> Tipos de identificador genérico grandes que são passados pelo valor podem ser manipulados somente por stubs de otimização <a href="-os.md"><strong>/os</strong></a> . Os stubs para essa rotina serão gerados usando a otimização de <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[allocate (all_nodes)] em um parâmetro [in, out] pode órfão a memória original</dt> <dd> O uso de [<a href="allocate.md"><strong>ALLOCATE</strong></a>(all_nodes)] em um parâmetro [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] deve realocar memória contígua para a direção [<strong>out</strong>], tornando-se órfão o parâmetro [<strong>in</strong>]. Esse uso não é recomendado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>Não é possível ter um ponteiro [REF] como um braço Union</dt> <dd> Os ponteiros de referência sempre devem apontar para memória válida, mas uma União [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] com um ponteiro de referência pode retornar um ponteiro de referência quando a direção [<strong>in</strong>] usava outro tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>retorno de identificadores de contexto sem suporte para modos/Oi, usando/os</dt> <dd> MIDL não dá suporte a identificadores de contexto nos modos de otimização totalmente interpretados. Alternando para a otimização de modo misto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>o uso do parâmetro [comm_status] ou [fault_status] extra não tem suporte para modos/Oi, usando/os</dt> <dd> Os atributos [<a href="comm-status.md"><strong>comm_status</strong></a>] e [<a href="fault-status.md"><strong>fault_status</strong></a>] só podem ser tratados por stubs de otimização <a href="-os.md"><strong>/os</strong></a> . Os stubs para essa rotina serão gerados usando a otimização de <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Não há suporte para o uso de um tipo desconhecido para [represent_as] ou [user_marshal] em modos/Oi, usando/os</dt> <dd> O uso do atributo [<a href="represent-as.md"><strong>represent_as</strong></a>] com um tipo local que não está definido no arquivo IDL ou um arquivo IDL importado só pode ser tratado por stubs de otimização <a href="-os.md"><strong>/os</strong></a> . Os stubs para essa rotina serão gerados usando a otimização de <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>tipos de matriz com [transmit_as] ou [represent_as] sem suporte no tipo de retorno para modos/Oi, usando/os</dt> <dd> O retorno de uma matriz com [<a href="transmit-as.md"><strong>transmit_as</strong></a>] ou [<a href="represent-as.md"><strong>represent_as</strong></a>] aplicado só pode ser tratado por stubs de otimização <a href="-os.md"><strong>/os</strong></a> . Os stubs para essa rotina serão gerados usando a otimização de <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>tipos de matriz com [transmit_as] ou [represent_as] não têm suporte passar por valor para modos/Oi, usando/os</dt> <dd> Essa ação não tem suporte para otimização totalmente interpretada. Alternando para a otimização de modo misto.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[callback] requer/ms_ext</dt> <dd> O atributo [<a href="callback.md"><strong>callback</strong></a>] é uma extensão da Microsoft e requer que a opção <a href="-ms-ext.md"><strong>/ms_ext</strong></a> seja habilitada. Não compile com <a href="-osf.md"><strong>/OSF</strong></a>, que substitui <strong>/ms_ext</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>dependência de interface circular</dt> <dd> Essa interface usa-se (direta ou indiretamente) como uma interface base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>somente IUnknown pode ser usado como a interface raiz</dt> <dd> Atualmente, todas as interfaces devem ter <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> como a interface raiz.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] só pode ser aplicado a ponteiros para interfaces</dt> <dd> O atributo [<a href="iid-is.md"><strong>iid_is</strong></a>] só pode ser aplicado a ponteiros de interface, embora possam ser especificados como ponteiros para <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>interfaces só podem ser usadas em constructos de ponteiro para interface</dt> <dd> Os nomes de interface não podem ser usados, exceto como interfaces base ou ponteiros de interface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>ponteiros de interface devem ter um UUID/IID</dt> <dd> O tipo base da expressão [<a href="iid-is.md"><strong>iid_is</strong></a>] deve ser um tipo UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>as definições e as declarações fora do corpo da interface exigem /ms_ext</dt> <dd> Colocar declarações e definições fora de qualquer corpo da interface é uma extensão da Microsoft e requer o uso da opção <a href="-ms-ext.md"><strong>/ms_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>várias interfaces em um arquivo exigem /ms_ext</dt> <dd> O uso de várias interfaces em um único arquivo idl é uma extensão da Microsoft e não está disponível quando você compila <a href="-osf.md"><strong>no modo /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>somente um dos [implicit_handle], [auto_handle] ou [explicit_handle] permitidos</dt> <dd> Cada interface pode ter apenas um desses três atributos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] faz referência a um tipo que não é um identificador</dt> <dd> Os alças implícitos devem ser de um dos tipos de alça.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>[object] procs só pode ser usado com &quot; /env win32&quot;</dt> <dd> Interfaces com o atributo [<a href="object.md"><strong>object</strong></a>] não podem ser usadas com ambientes de 16 bits.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[retorno de chamada] com -env dos/win16 sem suporte para /Oi, usando /Os</dt> <dd> Os retornos de chamada em ambientes de 16 bits só podem ser tratados por stubs <a href="-os.md"><strong>de otimização /SO.</strong></a> Os stubs dessa rotina serão gerados usando <strong>a otimização /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>float/double não tem suporte como parâmetro de nível superior para o modo /Oi, usando /Os</dt> <dd> Os tipos float e double só podem ser tratados como parâmetros pelos stubs <a href="-os.md"><strong>de otimização /Os.</strong></a> Os stubs dessa rotina serão gerados usando <strong>a otimização /Os.</strong> Os tipos float e double em estruturas, matrizes ou uniões ainda podem ser tratados com<strong>/Os</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>ponteiros para alças de contexto podem não ser usados como valores de retorno</dt> <dd> Os alças de contexto devem ser usados como valores de retorno diretos, não valores de retorno indiretos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>os procedimentos em uma interface de objeto devem retornar um HRESULT</dt> <dd> Todos os procedimentos em uma interface de objeto que não têm o atributo -[<a href="local.md"><strong>local</strong></a>] devem retornar um <strong>HRESULT</strong> / <strong>SCODE</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>UUID duplicada</dt> <dd> O mesmo que os UUIDs devem ser exclusivos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>As interfaces [object] devem derivar de outra interface [objeto], como IUnknown</dt> <dd> A herança de interface só é permitida quando você está usando interfaces de objeto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>A interface (assíncrona) deve derivar de outra interface (assíncrona)</dt> <dd> As interfaces de objeto, síncronas e assíncronas, devem derivar de <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> ou de alguma outra interface OLE base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>A expressão [IID_IS] deve ser um ponteiro para a estrutura IID</dt> <dd> O tipo base da expressão [<a href="iid-is.md"><strong>iid_is</strong></a>] deve ser um tipo UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as] o tipo deve ser um procedimento [local]</dt> <dd> O destino de um tipo [<a href="call-as.md"><strong>call_as</strong></a>] , se definido, deve ter [ <a href="local.md"><strong>local</strong></a>] aplicado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>indefinido [call_as] não deve ser usado em uma interface de objeto</dt> <dd> Você deve definir o destino de um tipo [<a href="call-as.md"><strong>call_as</strong></a>] . Certifique-se de ter fornecido <strong>call_as</strong> rotinas para os aplicativos de chamada e chamados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] não pode ser usado com [codificar] ou [decodificar]</dt> <dd> Os atributos [ <a href="encode.md"><strong>codificar</strong></a>] e [ <a href="decode.md"><strong>decodificar</strong></a>] só podem ser usados com alças explícitas ou alças implícitas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>Procedimentos normais não são permitidos em uma interface com [codificar] ou [decodificar]</dt> <dd> Interfaces que contêm procedimentos [<a href="encode.md"><strong>codificar</strong></a>] ou [<a href="decode.md"><strong>decodificar</strong></a>] também não podem ter procedimentos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>conformidade de nível superior ou variação não permitida com [codificação] ou [decodificar]</dt> <dd> Tipos que têm conformidade ou variação de nível superior não podem usar a serialização de tipo, pois não há como fornecer tamanho/alongamento. No entanto, as estruturas que as contêm têm permissão para usar a serialização de tipo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>Parâmetros [out] podem não ter &quot; const&quot;</dt> <dd> Como um parâmetro [<a href="out-idl.md"><strong>out</strong></a>] é alterado, ele não deve ser declarado como constante sa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>os valores de retorno podem não ter &quot; const&quot;</dt> <dd> Como um valor de função é definido quando a função retorna, esse valor não deve ser declarado como uma constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>uso inválido do &quot; atributo retval &quot;</dt> <dd> Verifique se você não usou o atributo [<a href="optional.md"><strong>opcional</strong></a>] e se o parâmetro [<a href="retval.md"><strong>retval</strong></a>] é o último parâmetro na lista.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>várias convenções de chamada ilícitas</dt> <dd> Somente uma convenção de chamada pode ser aplicada a um único procedimento.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>atributo ilegal no procedimento [objeto]</dt> <dd> O atributo acima só se aplica a procedimentos em interfaces que não têm o atributo [<a href="object.md"><strong>object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>Os ponteiros de interface [out] devem usar a indcisão dupla</dt> <dd> Como o valor alterado é o ponteiro para a interface, deve haver outro nível de indcisão acima do ponteiro para permitir que ele seja retornado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>procedimento usado duas vezes como o chamador em [call_as]</dt> <dd> Um determinado procedimento [<a href="local.md"><strong>local</strong></a>] pode ser usado apenas uma vez como o destino de um [<a href="call-as.md"><strong>call_as</strong></a>], a fim de evitar conflitos de nome.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[call_as] O destino deve ter [local] em uma interface de objeto</dt> <dd> O destino de um [<a href="call-as.md"><strong>call_as</strong></a>] deve ser um procedimento definido [<a href="local.md"><strong>local</strong></a>] na interface atual.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[código] e [nocode] não podem ser usados juntos</dt> <dd> Esses dois atributos são contraditórios e não podem ser usados juntos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>os procedimentos com atributos [talvez] ou [mensagem] podem não ter params [out] ou os valores de retorno devem ser do tipo HRESULT ou error_status_t</dt> <dd> Como os procedimentos [<a href="maybe.md"><strong>talvez</strong></a>] nunca retornam, não há como obter valores de retorno.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>ponteiro para função deve ser usado</dt> <dd> Embora as definições de tipo de função sejam permitidas no <a href="-c-ext.md"><strong>modo /c_ext,</strong></a> elas só podem ser usadas como ponteiros para funções. Eles nunca podem ser transmitidos como um parâmetro ou um valor de retorno de um procedimento remoto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>funções não podem ser passadas em uma operação RPC</dt> <dd> Funções e ponteiros de função não podem ser passados como parâmetros ou valores de retorno de procedimentos remotos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>Não há suporte para o Hyper/Double como valor de retorno para modos/Oi, usando/os</dt> <dd> Os valores de retorno de Hyper e Double só podem ser tratados por stubs de otimização <a href="-os.md"><strong>/os</strong></a> . Os stubs para essa rotina serão gerados usando a otimização de <strong>/os</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma Pack (pop) sem correspondência do pacote de #pragma (push)</dt> <dd> #pragma Pack (push) e pacote de #pragma (pop) devem aparecer em pares correspondentes. Pelo menos um número excessivo de pacotes de #pragma (push) foi especificado.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>os campos de estrutura com cadeia de caracteres devem ser byte/Char/wchar_t</dt> <dd> O tipo [<a href="string.md"><strong>String</strong></a>] só pode ser aplicado a uma estrutura cujos campos são todos do tipo byte ou uma definição de tipo equivalente a byte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[Notify] sem suporte para modos/Oi, usando/os</dt> <dd> O atributo [<a href="notify.md"><strong>Notify</strong></a>] só pode ser processado por stubs de otimização <a href="-os.md"><strong>/os</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> Não há suporte para o parâmetro de identificador ou tipo de retorno em um procedimento em uma interface [Object]</dt> <dd> Identificadores não podem ser usados com interfaces [ <a href="object.md"><strong>Object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C permite que a matriz mais à esquerda seja não especificada</dt> <dd> Em uma matriz compatível, o ANSI C permite que apenas a matriz mais à esquerda (mais significativa) seja não especificada. Se várias dimensões estiverem em conformidade, MIDL tentará colocar um &quot; 1 &quot; nas outras dimensões em conformidade. Se as outras dimensões forem definidas em uma definição de tipo diferente, isso não poderá ser possível. Tente colocar todas as dimensões da matriz na declaração de matriz para evitar isso. Em qualquer caso, tome cuidado com os cálculos de indexação de matriz feitos pelo compilador; Talvez seja necessário fazer seus próprios cálculos usando os tamanhos reais.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>parâmetros de União por valor sem suporte para modos/Oi, usando/os</dt> <dd> Essa ação não tem suporte para otimização totalmente interpretada. Alternando para a otimização de modo misto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>o atributo [Version] é ignorado em uma interface [Object]</dt> <dd> O atributo [<a href="object.md"><strong>Object</strong></a>] identifica uma interface com. Uma lista de atributos de interface para uma interface COM não pode incluir o atributo [ <a href="version.md"><strong>version</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>o atributo [size_is] ou [max_is] é inválido em uma matriz fixa</dt> <dd> Matrizes de tamanho fixo não podem usar os atributos <a href="size-is.md"><strong>size_is</strong></a> ou <a href="max-is.md"><strong>max_is</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[Encode] ou [decodificar] são inválidos em uma interface [Object]</dt> <dd> O atributo [<a href="object.md"><strong>Object</strong></a>] identifica uma interface com. Os atributos [<a href="encode.md"><strong>Encode</strong></a>] e [ <a href="decode.md"><strong>decodificar</strong></a>] habilitam a serialização. Ou seja, você pode fornecer e controlar buffers para marshaling e Unmarshal de dados. no entanto, não é possível executar a serialização em interfaces COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[codificar] ou [decodificar] em um tipo requer/ms_ext</dt> <dd> A serialização não faz parte da especificação de DCE-IDL. É uma extensão da Microsoft que requer o uso da opção de linha de comando <a href="-ms-ext.md"><strong>/ms_ext</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>int sem suporte em/env Win16 ou/env dos</dt> <dd> As plataformas Microsoft de 16 bits não oferecem suporte ao uso do tipo <a href="int.md"><strong>int</strong></a> em um arquivo IDL. Qualifique o tipo <strong>int</strong> com <a href="small.md"><strong>pequeno</strong></a>, <a href="short.md"><strong>curto</strong></a>ou <a href="long.md"><strong>longo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bString] só pode ser aplicado a um ponteiro para &quot; Char &quot; ou &quot; whchar_t&quot;</dt> <dd> Este erro está obsoleto. Ele é fornecido apenas para fins de compatibilidade com versões anteriores.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>atributo inválido em um procedimento em uma interface [Object]</dt> <dd> O atributo especificado não é permitido em um procedimento em uma interface COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>atributo inválido em uma interface [Object]</dt> <dd> O atributo especificado não é permitido em uma interface COM.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>muitos parâmetros ou pilha muito grandes para modos/Oi, usando/os</dt> <dd> Este aviso é obsoleto. Ele é fornecido apenas para fins de compatibilidade com versões anteriores. Isso indica que a chamada para o procedimento remoto faz com que a pilha cresça maior que 64 K.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>nenhum atributo no typedef do arquivo ACF, portanto, nenhum efeito</dt> <dd> O arquivo IDL deve conter todas as instruções TypeDef que não têm atributos. Eles não devem ocorrer em arquivos ACF. Se fizerem isso, o compilador MIDL os interpretará como redundante e os ignorará.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>chamadas de convenções diferentes de __stdcall ou __cdecl não têm suporte para modos/Oi, usando/os</dt> <dd> A chamada de convenções como <strong>__pascal</strong> ou <strong>__fastcall</strong> alterar o formato da pilha. Os modos <a href="-oi.md"><strong>/Oi</strong></a> só dão suporte às convenções de chamada <strong>__stdcall</strong> e <strong>__cdecl</strong> . Se você precisar usar outras convenções de chamada, use o modo <a href="-os.md"><strong>/os</strong></a> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>muitos métodos de delegação na interface, exigem Windows 2000 ou superior</dt> <dd> Uma interface pode herdar de outra. Quando ele faz isso, os métodos da interface base são considerados delegados. Nenhuma interface derivada pode conter mais de 256 métodos delegados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>identificadores automáticos não têm suporte com/env Mac ou/env PowerMac</dt> <dd> Ao compilar seu arquivo IDL para um PowerMac, você não pode usar identificadores de ligação automática. Você deve especificar identificadores explícitos ou implícitos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>as instruções fora do bloco de biblioteca são ilegais no modo de compatibilidade MkTypLib</dt> <dd> Talvez seja necessário especificar a opção de linha de comando <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> ao compilar o arquivo IDL.<br/>
<blockquote>
[!Note]<br />
A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>sintaxe inválida, a menos que use o modo de compatibilidade MkTypLib</dt> <dd> Talvez seja necessário especificar a opção de linha de comando <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> ao compilar o arquivo IDL.<br/>
<blockquote>
[!Note]<br />
A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Definição inválida, deve usar typedef no modo de compatibilidade MkTypLib</dt> <dd> Talvez seja necessário especificar a opção de linha de comando <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> ao compilar o arquivo IDL.<br/>
<blockquote>
[!Note]<br />
A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>atributo de ponteiro explícito [ptr] [ref] ignorado para ponteiros de interface</dt> <dd> Ponteiros para interfaces não podem ter atributos IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td><a href="-oi.md"><strong>/Modos de Oi</strong></a> não implementados para o PowerMac, alternando para <a href="-os.md"> <strong>/Os</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>Tipo de expressão ilegal usado no atributo</dt> <dd> O valor padrão do ponteiro deve ser uma constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>Tipo ilegal usado no pipe</dt> <dd> Os pipes são limitados a tipos de dados IDL básicos. Por exemplo, você não pode especificar um pipe de matrizes.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>O procedimento usa pipes, usando /Oicf</dt> <dd> O modo selecionado não dá suporte a pipes. O compilador MIDL detectou o uso de um ou mais pipes em sua interface. Portanto, ele está compilando o arquivo IDL no <a href="-oi.md"><strong>modo /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>o procedimento tem um atributo que requer o uso de /Oif, alternando modos</dt> <dd> Você deve compilar procedimentos [<a href="async.md"><strong>assíncronos</strong></a>] no <a href="-oi.md"><strong>modo /Oif.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>requisitos de otimização conflitantes, não é possível otimizar</dt> <dd> Esse erro geralmente indica que você especificou <a href="-os.md"><strong>/Os</strong></a> e <a href="-oi.md"><strong>/Oi</strong></a> (ou uma variante dos modos de compilador <strong>/Oi</strong>) MIDL. Isso também pode significar que os recursos especificados nos arquivos IDL e ACL exigem o uso de ambos os modos. Você deve selecionar um modo ou outro para otimizar.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>pipes não podem ser elementos de matriz ou membros de estruturas ou uniões</dt> <dd> Os tipos de dados de pipe só podem ser parâmetros de nível superior.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>uso de pipe inválido</dt> <dd> Não é possível usar pipes com os atributos [<a href="transmit-as.md"><strong>transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>], ou [<a href="user-marshal.md"><strong>user_marshal</strong></a>] . Além disso, os pipes não podem ser usados como tipos de retorno.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>O recurso requer a opção de otimização interpretada avançada; use -Oicf</dt> <dd> Esse erro indica que as opções de linha de comando do compilador MIDL, como <a href="-robust.md"><strong>/robust,</strong></a> exigem o uso do <a href="-oi.md"><strong>modo /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>O recurso requer a opção de otimização interpretada avançada; use -Oicf</dt> <dd> Esse aviso indica que as opções de linha de comando do compilador MIDL, como <a href="-robust.md"><strong>/robust,</strong></a> exigem o uso do <a href="-oi.md"><strong>modo /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>a opção de otimização está sendo em fases, use -Oic</dt> <dd> O <a href="-oi.md"><strong>modo de otimização /Oi1</strong></a> foi especificado na linha de comando MIDL. Esse modo não tem mais suporte e <strong>/Oicf</strong> deve ser usado em vez disso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>a opção de otimização está sendo em fases, use -Oicf</dt> <dd> O <a href="-oi.md"><strong>modo de otimização /Oi2</strong></a> foi especificado na linha de comando MIDL. Esse modo não tem mais suporte e <strong>/Oicf</strong> deve ser usado em vez disso.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>a opção de otimização está sendo em fases, use -ic</dt> <dd> O modo de otimização i1 foi especificado em um atributo ACF [optimize]. Esse modo não tem mais suporte e o icf deve ser usado em vez disso.<br/> Exemplo de arquivo ACF:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>a opção de otimização está sendo em fases, use -icf</dt> <dd> O modo de otimização i2 foi especificado em um atributo ACF [optimize]. Esse modo não tem mais suporte e o icf deve ser usado em vez disso.<br/> Exemplo de arquivo ACF:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>as opções -old e -new estão obsoletas, use -oldtlb e -newtlb</dt> <dd> Essa mensagem está obsoleta e não é mais omitida pelo MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>Valor do argumento ilegal</dt> <dd> As variantes permitidas da opção de linha de comando /O incluem <a href="-os.md"><strong>/Os</strong></a>, <a href="-oi.md"><strong>/Oi</strong></a>, <strong>/Oic</strong>, <strong>/Oicf</strong>e <strong>/Oif</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>Tipo de expressão ilegal em constante</dt> <dd> A expressão não é avaliada como uma constante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>Tipo de expressão ilegal em enum</dt> <dd> Um valor enumerado em uma <a href="enum.md"><strong>definição de enumeração</strong></a> não é avaliada como um tipo integral.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>declaração de encaminhamento não satisfeita</dt> <dd> O compilador MIDL não pôde resolver a definição de uma declaração de encaminhamento.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>as opções são contraditórias</dt> <dd> Você não pode usar as opções de linha de comando <a href="-osf.md"><strong>/osf</strong></a> <a href="-ms-ext.md"><strong>e /ms_ext</strong></a> ao compilar um arquivo IDL. Você deve escolher um ou outro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL não pode gerar informações HOOKOLE para a união não capaz de rpc</dt> <dd> Esse erro está obsoleto. Ele é fornecido estritamente para compatibilidade com backward.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>nenhuma expressão de caso encontrada para união</dt> <dd> Cada campo de uma união deve ter uma instrução case com uma expressão constante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] e [wire_marshal] não são suportados com sinalizadores -Oi e -Oic, use -Os ou -Oicf</dt> <dd> Os atributos [<a href="user-marshal.md"><strong>user_marshal</strong></a>] e [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] exigem os recursos de otimização específicos disponíveis somente em <a href="-oi.md"><strong>/Oicf</strong></a> (proxy sem código com cadeias de caracteres de formato rápido) ou <a href="-os.md"><strong>/Os</strong></a> (marshaling de modo misto).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>Pipes não podem ser usados com serialização de dados, ou seja, [codificar] e/ou [decodificar]</dt> <dd> Não é possível passar pipes como parâmetros para procedimentos que têm os atributos [<a href="encode.md"><strong>codificar</strong></a>] ou [<a href="decode.md"><strong>decodificar</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>todos os ponteiros de interface de pipe devem usar uma única indcisão</dt> <dd> Não é possível usar um ponteiro para um ponteiro para uma interface de pipe dessa maneira.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is()] não pode ser usado com um ponteiro de interface de pipe</dt> <dd> Essa mensagem está obsoleta. Essa mensagem não é mais usada pelo compilador.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>opção -lcid inválida ou inaplicável</dt> <dd> O LCID (identificador local) especificado não é válido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>o lcid especificado é diferente da especificação anterior</dt> <dd> Os valores especificados em /lcid e [<a href="lcid.md"><strong>lcid</strong></a>] são diferentes. O compilador MIDL usará o último definido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>importlib não é permitido fora de um bloco de biblioteca</dt> <dd> Todas as instruções<a href="importlib.md"><strong>[ importlib</strong></a>] devem ocorrer em um bloco [<a href="library.md"><strong>biblioteca</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>valor de ponto flutuante inválido</dt> <dd> Esse erro não deve ser emitido pelo MIDL. Se você vir esse erro, informe um bug à Microsoft fornecendo todos os arquivos necessários para reproduzir o erro, incluindo seus arquivos IDL, arquivos ACF, headers etc.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>membro inválido</dt> <dd> Os procedimentos não podem ser membros de uma biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>membro inválido possível</dt> <dd> Para ser um membro válido de uma biblioteca, o elemento de biblioteca deve ser um módulo, uma dispinterface, uma coclasse, uma instrução if, uma estrutura, uma união, uma enumeração ou uma declaração de encaminhamento.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>incompatibilidade em tipos de pipe e interface</dt> <dd> Essa mensagem está obsoleta.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>cadeia de caracteres, matriz variável, matriz compatível e parâmetros de ponteiro completo podem ser incompatíveis com parâmetros de pipe durante o tempo de operação</dt> <dd> Um método que combina uma ou mais cadeias de caracteres [in], matrizes variáveis, matrizes compatíveis e parâmetros de ponteiro completo e qualquer parâmetro de pipe [in] resulta na geração de um stub que é executado somente em sequências de protocolo <strong>ncacn_*</strong> e <a href="ncalrpc.md"><strong>ncalrpc</strong></a> em computadores Windows. Usar o stub para fazer chamadas em sequências de <strong>protocolo ncadg_*</strong> ou aceitar chamadas de outros fornecedores de RPC DCE do OSF pode gerar falhas no servidor durante o tempo de operação. Esse erro ocorre a partir do Windows Server 2003.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>O parâmetro deve estar em</dt> <dd> Os alças assíncronas devem ser parâmetros [<a href="in.md"><strong>em</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>o tipo de parâmetro de um objeto [assíncrono] deve ser um ponteiro duplo para uma interface</dt> <dd> O parâmetro deve ser do tipo <strong>IAsyncManager</strong> **.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>tipo de identificador assíncrono incorreto</dt> <dd> O tipo de identificador deve ser <strong>IAsyncManager</strong> ou um tipo derivado de <strong>IAsyncManager.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>a &quot; opção &quot; interna habilita recursos sem suporte, use com cuidado</dt> <dd> Evite usar essa opção.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>Os procedimentos assíncrono não podem usar o manipular automaticamente</dt> <dd> Os procedimentos com o atributo [<a href="async.md"><strong>assíncrono</strong></a>] exigem alças explícitas.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t deve ter [comm_status] e [fault_status]</dt> <dd> Um procedimento foi especificado com os atributos IDL [talvez] ou [mensagem], mas o tipo de retorno tem apenas os atributos ACF [comm_status] ou [fault_status]. Ambos os atributos do ACF são necessários.<br/> Exemplo de arquivo ACF:<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>esse constructo só é permitido dentro de um bloco de biblioteca</dt> <dd> Um módulo só pode ocorrer dentro de um bloco de biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>redefinição de tipo inválido</dt> <dd> Um novo tipo foi definido recursivamente em um tipo inexistente.<br/> Exemplo:<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>os procedimentos com um atributo [vararg] devem ter um parâmetro SAFEARRAY(VARIANT); param order is [vararg], [lcid], [retval]</dt> <dd> A maioria dos parâmetros para procedimentos com o atributo [<a href="vararg.md"><strong>vararg</strong></a>] deve ocorrer antes do <strong>parâmetro SAFEARRAY(VARIANT).</strong> O <strong>parâmetro SAFEARRAY(VARIANT)</strong> deve estar presente. Se a lista de parâmetros contiver um parâmetro com o atributo [ <a href="lcid.md"><strong>lcid</strong></a>], ele deverá seguir o <strong>parâmetro SAFEARRAY(VARIANT).</strong> Se a lista de parâmetros contiver um parâmetro com o atributo [<a href="retval.md"><strong>retval</strong></a>], ele deverá ocorrer após o parâmetro com o atributo [<strong>lcid</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>muitos métodos na interface exigem Windows 2000 ou superior</dt> <dd> O compilador MIDL não permite mais de 1024 métodos em uma interface quando você está compilando no <a href="-oi.md"><strong>modo /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>switch está sendo eliminado em fases</dt> <dd> As opções a seguir são obsoletas: /<strong>hookole</strong>, /<strong>env win16</strong>e<strong>/env</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>não pode derivar de IAdviseSink, IAdviseSink2 ou IAdviseSinkEx</dt> <dd> Essas interfaces não podem ser estendidas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>não pode atribuir um valor padrão</dt> <dd> A atribuição de um valor padrão a um parâmetro é permitida Visual Basic, mas não no C++. Se você estiver usando o C++, o valor padrão será ignorado.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>Não há suporte para a geração de biblioteca de tipos para DOS/Win16/MAC</dt> <dd> MIDL não dá suporte a bibliotecas de tipo de 16 bits.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>erro ao gerar a biblioteca de tipos, ignorada</dt> <dd> Ocorreu um erro não fatal ao gerar a biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>tamanho da pilha excedido para /Oi, usando /Os</dt> <dd> O modo de otimização -Oi é limitado a 128 bytes de espaço de pilha para parâmetros. O compilador alternou automaticamente para o modo de otimização do sistema operacional para resolver essa limitação.<br/> Para evitar esse aviso, use os modos de otimização -Oicf ou -Os. O modo de otimização pode ser alterado na linha de comando especificando -Oicf ou -Os em vez de -Oi ou adicionando um atributo [optimize9 &quot; icf )] ou optimize[s )] à função no arquivo &quot; &quot; &quot; ACF.<br/> Esse aviso normalmente ocorre ao passar estruturas grandes como parâmetros por valor. O tamanho da pilha necessário pode ser reduzido passando um ponteiro para a estrutura.<br/> Exemplo:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>O uso de /robust requer /Oicf, alternando modos</dt> <dd> Você deve compilar no <a href="-oi.md"><strong>modo /Oicf</strong></a> ao especificar a <a href="-robust.md"><strong>opção /robust</strong></a> na linha de comando.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>intervalo incorreto especificado</dt> <dd> O valor mais alto especificado em um atributo [<a href="range.md"><strong>intervalo</strong></a>] é menor que o valor mais baixo.<br/> Exemplo:<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> combinação inválida de parâmetros [in] somente e [out] para a interface [async_uuid]</dt> <dd> Somente combinações simples de atributos com parâmetros [<a href="in.md"><strong>in</strong></a>] ou [<a href="out-idl.md"><strong>out</strong></a>] são permitidas para esse tipo de interface.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>As plataformas DOS, Win16 e MAC não têm suporte com /robust</dt> <dd> O MIDL dá suporte à <a href="-robust.md"><strong>opção /robust</strong></a> no Microsoft Windows 2000 ou posterior.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>O suporte para proxies de stubless de estilo NT 3.51 para interfaces de objeto será eliminado em fases; use /Oif.</dt> <dd> Esse modo está obsoleto. Use <a href="-oi.md"><strong>/Oif</strong></a> ou <strong>/Oicf</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[codificar] ou [decodificar] com /robust requer /Oicf</dt> <dd> A serialização não pode ser executada quando a <a href="-robust.md"><strong>opção /robust</strong></a> é especificada.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>atributos conflitantes especificados</dt> <dd> [<a href="context-handle-serialize.md"><strong>context_handle_serialize</strong></a>] e [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>] foram especificados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[serialize], [naerialize] pode ser aplicado a context_handles</dt> <dd> Os atributos ACF [context_handle_serialize] ou [context_handle_noserialize] só podem ser aplicados a tipos que são alças de contexto.<br/> Exemplo de arquivo IDL:<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
Exemplo de arquivo ACF:<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>O compilador atingiu um limite para uma representação de cadeia de caracteres de formato. Consulte a documentação para ver os conselhos.</dt> <dd> O compilador MIDL tem um limite de 64 KB para cadeias de caracteres de formato. Esse erro geralmente ocorre quando arquivos IDL incluem outros arquivos IDL. O arquivo IDL composto gerado por todas as instruções include excede os limites das tabelas de representação de tipo do interpretador do mecanismo de marshaling. Tente usar a diretiva import em vez da diretiva include em seus arquivos IDL. Para obter mais informações, <a href="importing-system-header-files.md">consulte Importando arquivos de header do sistema,</a> <a href="include.md"><strong>incluir</strong></a>e <a href="import.md"><strong>importar</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>O formato wire pode estar incorreto, talvez seja necessário usar -ms_conf_struct, consulte a documentação para saber mais</dt> <dd> O compilador MIDL não pôde gerar um formato permitido para os dados. Uma maneira comum de obter esse erro é definir um <strong>ms_conf_struct</strong> dentro de uma estrutura complexa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>um tamanho de pilha ou um deslocamento maior que o limite de 64 K. Consulte a documentação para ver os conselhos.</dt> <dd> A chamada resulta em uma pilha maior que 64 KB. Tente passar os dados em blocos menores.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>um modo de interpretador forçado para plataforma de 64 bits </dt> <dd> Plataformas de 64 bits exigem o modo de compilação /Oicf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>O tamanho do elemento da matriz é maior que o limite de 64 KB.</dt> <dd> Todos os elementos de matriz devem ter menos de 64 KB de tamanho.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>pode haver apenas um parâmetro [Icid] em um método e ele deverá ser o último ou o segundo a ser o último se o último parâmetro tiver [retval]</dt> <dd> Um parâmetro com o atributo [<a href="lcid.md"><strong>lcid</strong></a>] deve ocorrer por último. A única exceção é quando também há um parâmetro com o atributo [<a href="retval.md"><strong>retval</strong></a>]. Quando ambos ocorrem, o segundo para o último parâmetro na lista de parâmetros deve ter o atributo [ <strong>lcid</strong>]. O último parâmetro deve ter o atributo [<strong>retval</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>sintaxe incorreta para midl_pragma</dt> <dd> O compilador MIDL detectou um erro de sintaxe desconhecido em uma midl_pragma de dados.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 há suporte no modo /osf</dt> <dd> Se você precisar usar __int3264, compile no modo /ms-ext.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>símbolo não resolvido na biblioteca de tipos</dt> <dd> O compilador não pôde resolver uma declaração formal ou um tipo referenciado na biblioteca de tipos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>Pipes assíncronos não podem ser passados por valor</dt> <dd> Os pipes assíncronos devem ser passados por referência ou por endereço.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>O deslocamento de parâmetro excede o limite de 64 KB para procedimentos interpretados</dt> <dd> Esse erro normalmente significa que um procedimento tem muitos parâmetros.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>elemento de matriz inválido</dt> <dd> Pipes não podem ser usados como elementos de matriz.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>Os membros dispinterface devem ser métodos, propriedades ou interfaces</dt> <dd> Uma dispinterface não pode conter definições de tipo, estruturas, enumerações ou uniões.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>Procedimento [local] sem [call_as]</dt> <dd> Os procedimentos de objeto que têm o atributo [<a href="local.md"><strong>local</strong></a>] também exigem o atributo [<a href="call-as.md"><strong>call_as</strong></a>] .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>vetor multidimensional, alternando para /Oicf</dt> <dd> O <a href="-os.md"><strong>modo de otimização</strong></a> /Os não dá suporte a matrizes de tamanho não fixas multidimensionais. O compilador alternou automaticamente o modo de otimização para<strong>/Oicf</strong> para essa função. <br/> Esse aviso pode ser suprimido globalmente alterando o modo do compilador especificando/Oicf na linha de comando MIDL ou usando <strong>midl_pragma</strong> aviso (desabilitar: 2393) no arquivo IDL.<strong></strong> O modo de otimização pode ser alterado para uma função individual adicionando o atributo [<strong>optimize( &quot; icf &quot; )</strong>] à função no arquivo ACF.<br/> O exemplo a seguir demonstra este aviso:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>tipo ou constructo sem suporte em um bloco de biblioteca porque Oleaut32.dll suporte para tipos polimórficos de 64 KB está ausente</dt> <dd> A automação OLE não dá suporte a tipos polimórficos (como _int3264, INT_PTR etc. Esses tipos têm representações de dados incompatíveis entre plataformas de 32 e 64 bits. A chamada remota falhará em tempo de operação em plataformas de 64 bits.<br/>
<blockquote>
[!Note]<br />
Observe que, Windows versão 2000, os arquivos TLB de 64 bits são suportados pela Automação OLE convertendo informações de TLB de 32 bits em tempo de executar. Portanto, somente a geração TLB de 32 bits é suportada pelo MIDL.
</blockquote>
<br/> Se MIDL estiver sendo usado apenas para gerar um arquivo de header, a opção <a href="-notlb.md"><strong>/notlb</strong></a> suprimirá a geração do arquivo TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>código do interpretador antigo que está sendo gerado para 64b</dt> <dd> Esse erro está obsoleto. Se você vir esse erro, informe um bug para a Microsoft, dando seus arquivos IDL, arquivos ACF e linha de comando MIDL completa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>não há mais suporte para a opção do compilador</dt> <dd> Não há mais suporte para a opção ou as opções especificadas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>não pode executar o mecanismo MIDL</dt> <dd> A partir da versão Windows 2000 (VERSÃO MIDL 5.03.279), o compilador MIDL é implementado usando dois arquivos executáveis: Midl.exe (o driver) e Midlc.exe (o mecanismo do compilador). Esse erro indica que o Midl.exe não é capaz de iniciar Midlc.exe. Certifique-se de Midlc.exe no mesmo diretório que Midl.exe e se eles são da mesma versão.<br/> O erro pode ter sido causado pela cópia Midl.exe, mas não Midlx.exe da distribuição mais recente. Execute <strong>midl</strong> e/ou <strong>midlc</strong> na linha de comando sem parâmetros para ver o número de versão do executável.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>comandos ruins do driver</dt> <dd> A partir da versão Windows 2000 (VERSÃO MIDL 5.03.279), o compilador MIDL é implementado usando dois arquivos executáveis: Midl.exe (o driver) e Midlc.exe (o mecanismo do compilador). Esse erro indica que o arquivo temporário usado para passar comandos de Midl.exe para Midlc.exe está ausente ou corrompido. Certifique-se de Midlc.exe no mesmo diretório que Midl.exe e se eles são da mesma versão.<br/> O erro pode ter sido causado pela tentativa de executar Midlc.exe diretamente ou copiando Midl.exe, mas não Midlc.exe da distribuição mais recente. Execute <strong>midl</strong> e/ou <strong>midlc</strong> na linha de comando sem parâmetros para ver o número de versão do executável.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>para a automação OLE, os parâmetros opcionais devem ser VARIANT ou VARIANT *</dt> <dd> A automação OLE requer que todos os parâmetros [optional] sejam do tipo <strong>Variant</strong> ou <strong>Variant *</strong>.<br/> Na automação OLE, o uso de parâmetros não VARIAntes pode fazer com que a chamada falhe em tempo de execução ou passe dados indefinidos para os parâmetros [<a href="optional.md"><strong>optional</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[DefaultValue] é aplicado a uma não variante e [opcional]. Remova [opcional]</dt> <dd> O atributo [<a href="defaultvalue.md"><strong>DefaultValue</strong></a>] implica [<a href="optional.md"><strong>opcional</strong></a>]. O atributo [ <strong>optional</strong>] não é necessário.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>o atributo [opcional] não é aplicável fora de um bloco de biblioteca</dt> <dd> A funcionalidade implícita pelo atributo [ <a href="optional.md"><strong>opcional</strong></a>] não é aplicável a proxies gerados para uma interface fora de um bloco de biblioteca.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>O tipo de dados do parâmetro [ICID] deve ser longo</dt> <dd> A automação OLE requer que os parâmetros com o atributo [<strong>ICID</strong>] devam ser do tipo <a href="long.md"><strong>Long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>os procedimentos com [propput], [propget] ou [propref] não podem ter mais de um parâmetro necessário após [optional] One</dt> <dd> Não pode haver mais de um parâmetro sem [<a href="optional.md"><strong>optional</strong></a>] após o último parâmetro com [<strong>optional</strong>] ao usar [<a href="propput.md"><strong>propput</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] ou [ <a href="propputref.md"><strong>propputref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] ou [fault_status] com escolha necessária-Oicf</dt> <dd> O modo de otimização antigo-<strong>Oi</strong> não dá suporte a procedimentos ou parâmetros com [ <a href="comm-status.md"><strong>comm_status</strong></a>] ou [ <a href="fault-status.md"><strong>fault_status</strong></a>] com seleção (ou seja, usando [ <a href="encode.md"><strong>Encode</strong></a>] e/ou [ <a href="decode.md"><strong>decodificar</strong></a>]).<br/> Esse aviso pode ser suprimido globalmente especificando-<strong>Oicf</strong> na linha de comando MIDL ou em uma função individual adicionando o atributo [Optimize ( &quot; ICF:)] à função no arquivo ACF.<br/> Em geral, o modo de otimização do-<strong>Oicf</strong> é recomendado no modo mais de-<strong>Oi</strong> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>incompatibilidade da versão do driver MIDL e do compilador</dt> <dd> a partir da versão Windows 2000 (MIDL versão 5.03.279), o compilador MIDL é implementado usando dois arquivos executáveis: Midl.exe (o driver) e Midlc.exe (o mecanismo do compilador). Esse erro indica que a versão do Midl.exe não corresponde à versão do Midlc.exe.<br/> O erro pode ter sido causado pela cópia de Midl.exe, mas não Midlc.exe da distribuição mais recente. Execute <strong>MIDL</strong> e/ou <strong>midlc</strong> na linha de comando sem parâmetros para ver o número de versão do executável.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>nenhum arquivo intermediário especificado: Use Midl.exe</dt> <dd> a partir da versão Windows 2000 (MIDL versão 5.03.279), o compilador MIDL é implementado usando dois arquivos executáveis: Midl.exe (o driver) e Midlc.exe (o mecanismo do compilador). Esse erro indica que Midlc.exe foi executado diretamente em vez de usar Midl.exe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>problema de processamento com um parâmetro em um procedimento</dt> <dd> Esse erro pode ser visto durante a importação de dados de um TLB e quando um procedimento tem um parâmetro inválido. <br/> Se você vir esse erro, relate um bug à Microsoft. Especifique os arquivos IDL, os arquivos ACF, o arquivo TLB e a linha de comando MIDL completa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>problema de processamento com um campo em uma estrutura</dt> <dd> Esse erro pode ser visto durante a importação de dados de um TLB e quando uma estrutura tem um campo de estrutura ou União inválido.<br/> Se você vir esse erro, relate um bug à Microsoft. Especifique os arquivos IDL, os arquivos ACF, o arquivo TLB e a linha de comando MIDL completa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>inconsistência de compilador interna detectada: o deslocamento da cadeia de formato é inválido. Consulte a documentação para obter mais informações.</dt> <dd> O compilador MIDL detectou um valor inválido em suas estruturas de dados internas. Isso pode ser causado por estruturas que são recursivas ou por compilador violando seus próprios limites de representação para dados internos. Para identificar e/ou solucionar o problema, tente simplificar o arquivo IDL. Você pode fazer isso simplificando parâmetros complexos e estruturas de dados recursivas ou tornando o arquivo IDL menor, dividindo-o. Essa mensagem pode ser acompanhada por uma impressão de diagnóstico com informações adicionais sobre o problema.<br/> Se você vir esse erro, relate um bug à Microsoft. Especifique os arquivos IDL, os arquivos ACF, a linha de comando MIDL completo e a saída de diagnóstico, se houver.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>inconsistência de compilador interno detectada: o deslocamento de tipo é inválido. Consulte a documentação para obter mais informações.</dt> <dd> O compilador MIDL detectou um valor inválido em suas estruturas de dados internas. Isso pode ser causado por estruturas que são recursivas ou pelo compilador que viola seus próprios limites de representação para dados internos. Para identificar e/ou solucionar o problema, tente simplificar o arquivo IDL. Você pode fazer isso simplificando parâmetros complexos e estruturas de dados recursivas ou tornando o arquivo IDL menor, dividindo-o. Essa mensagem pode ser acompanhada por uma impressão de diagnóstico com informações adicionais sobre o problema.<br/> Se você vir esse erro, relate um bug à Microsoft. Especifique os arquivos IDL, os arquivos ACF, a linha de comando MIDL completo e a saída de diagnóstico, se houver.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>A sintaxe de SAFEARRAY (Roo) não tem suporte fora do bloco de biblioteca, use LPSAFEARRAY para proxy</dt> <dd> SAFEARRAYs tipados explicitamente não são permitidos fora de um bloco de biblioteca. Use LPSAFEARRAY em vez disso.<br/> O exemplo a seguir demonstra esse erro:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>Não há suporte para campos de bits</dt> <dd> Os campos de bits de estilo C não são suportados pelo MIDL. Isso se aplica à geração de proxy, bem como à geração de TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>Não há suporte para pontos flutuantes ou tipos de retorno complexos com [decodificar] em-Oicf, usando-OI</dt> <dd> Os procedimentos com tipos de retorno de ponto flutuante ou estrutura/União não têm suporte na escolha de estilo-Oicf. Uma solução alternativa para 32 bits é usar o modo de otimização-Oi ao serializar dados (usando [Encode] e/ou [decodificar]). no entanto, como o interpretador de estilo antigo-Oi e o suporte de seleção são destacados para serem divididos após a versão Windows 2000, o uso de ponteiros é altamente sugerido como solução para esse problema. Observe também que, normalmente, alterar um método de interface para usar um ponteiro [out, REF] em vez do valor de retorno que está causando o problema é totalmente compatível com versões anteriores no fio e pode ser facilmente ocultado da camada de aplicativo. <br/> Esse aviso pode ser suprimido globalmente, especificando-Oi na linha de comando MIDL ou em uma função individual, adicionando o atributo [Optimize ( &quot; i &quot; )] à função no arquivo ACF.<br/> O exemplo a seguir demonstra o problema:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Uma opção para contornar essa limitação seria passar um parâmetro [out] para manter o resultado em vez de usar um valor de retorno:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Como mencionado anteriormente, a solução descrita acima é boa, não apenas para as novas interfaces, mas também como solução alternativa para as antigas. A representação de transmissão para o &quot; novo &quot; argumento out é a mesma que para o valor de retorno (Observe void como o novo valor de retorno).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>Não há suporte para o tipo de retorno de 64 bits ao usar [decodificar]</dt> <dd> Os procedimentos com pontos flutuantes ou tipos de retorno de estrutura/União não têm suporte no modo de 64 bits ao executar a serialização de dados (usando [ <a href="encode.md"><strong>Encode</strong></a>] e/ou [ <a href="decode.md"><strong>decodificar</strong></a>]). Isso está relacionado ao estilo antigo – o intérprete Oi e o serializador de dados não têm suporte na plataforma de 64 bits. Consulte a descrição de MIDL2414 para obter mais informações. <br/> O exemplo a seguir demonstra esse erro:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
O seguinte é aconselhado como uma solução alternativa para interfaces novas e antigas. Use um parâmetro [out] para manter o resultado em vez de usar um valor de retorno:<br/> Roo. idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
Roo. ACF: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Observe que essa solução é totalmente compatível com versões anteriores na conexão, pois a representação de transmissão de um ponteiro [REF, out] ou um Double é a mesma que a de um Double.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>o tipo transmitido não pode conter um ponteiro completo para [wire_marshal] ou [user_marshal]</dt> <dd> Os tipos com atributos [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] ou [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] não podem conter ponteiros completos ([ <strong>PTR</strong>]). Use [ <a href="unique.md"><strong>Unique</strong></a>] ou [ <a href="ref.md"><strong>ref</strong></a>] em vez disso.<br/> O exemplo a seguir demonstra esse erro:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>O tipo transmitido deve ser um ponteiro ou ter um tamanho constante para [wire_marshal] e [user_marshal]</dt> <dd> Os tipos de nível superior com atributos [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] ou [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] devem ter um tamanho bem definido no tempo de compilação. Eles não podem ser ou conter matrizes compatíveis ou de tamanhos variados.<br/> O exemplo a seguir demonstra esse erro:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>os procedimentos com [propget] devem ter pelo menos um parâmetro ou um valor de retorno</dt> <dd> Os procedimentos com o atributo [propget] devem ter algum meio de retornar o valor da propriedade. Eles devem ter pelo menos um parâmetro [<a href="-out.md"><strong>out</strong></a>] ou um valor de retorno.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>O atributo [readonly] foi aplicado no nível do método.</dt> <dd> O atributo [somente leitura] só pode ser aplicado no nível do parâmetro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>As estruturas que contêm matrizes compatíveis devem ser passadas por referência</dt> <dd> Os parâmetros de nível superior no RPC devem ter um tamanho bem definido no tempo de compilação. Eles não podem ser, nem contêm matrizes compatíveis ou de tamanho variável. Além disso, os usuários não podem codificar/decodificar um tipo sem um tamanho bem definido. Os aplicativos precisam passar struct compatível/struct variável compatível por referência.<br/> O exemplo a seguir demonstra esse erro:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> problema interno do <system error code> - compilador que o compilador não pode continuar por um motivo desconhecido. Consulte a documentação para ver uma solução alternativa.</dt> <dd> O compilador não pôde continuar e a causa do erro é desconhecida. O número de erro hexadecimal é um identificador de erro do sistema. A compilação pode ter falhado devido a um problema externo, como uma condição de falta de memória. Nesse caso, você pode encontrar mais informações em Winerror.h ou Ntstatus.h. <br/> Há duas situações que geralmente geram esse erro:<br/>
<ul>
<li>O compilador MIDL não conseguiu se recuperar depois de detectar um erro no arquivo IDL. Se MIDL retornou mensagens de erro sobre o arquivo IDL, tente corrigi-las e recompilar. Se não houver mensagens de erro, o compilador poderá ter falhado antes de relatar um erro. Procure um erro de sintaxe na linha para a qual o erro interno do compilador é relatado.</li>
<li>O compilador MIDL não pôde gerar o código correto em uma opção de otimização especificada. Tente alterar os modos do compilador, compilando em otimização de modo misto<a href="-os.md"><strong>(/so)</strong></a>ou removendo todas as otimizações. Ou recompile usando o sinalizador /NO_FORMAT_OPT para suprimir a otimização padrão de procedimento e descritores de tipo do MIDL.</li>
</ul>
Ocasionalmente, esse erro ocorre mesmo quando o arquivo IDL está correto e nenhuma opção de otimização está sendo usada. Se esse for o caso, tente reescrever a seção de código nas proximidades de onde o erro foi relatado removendo quaisquer modificações recentes, simplificando ou reorganizando tipos de dados, alterando protótipos ou comece a comentar partes do arquivo IDL para localizar o código do problema.<br/> Se nenhuma dessas opções funcionar ou se você achar que o problema pode estar relacionado a um bug no Midl.exe, notifique a Microsoft, dando todos os detalhes relevantes.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

