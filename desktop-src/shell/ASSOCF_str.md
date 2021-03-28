---
description: Fornece informações para os métodos de interface IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumeração ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172533"
---
# <a name="assocf-enumeration"></a>Enumeração ASSOCF

Fornece informações para os métodos de interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .

## <a name="syntax"></a>Syntax

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th>C++</th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a>Constantes

 <span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ nenhum** 

Nenhuma das opções a seguir está definida.

 <span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID** 

Instrui os métodos de interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) a não mapear valores CLSID para valores de ProgID.

 <span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME** 

Identifica o valor do parâmetro *pwszAssoc* de [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) como um nome de arquivo executável. Se esse sinalizador não for definido, a chave raiz será definida como o ProgID associado à chave **. exe** em vez do ProgID do arquivo executável.

 <span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ abrir \_ BYEXENAME** 

Idêntico a **ASSOCF \_ init \_ BYEXENAME**.

 <span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR** 

Especifica que quando um método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) não encontra o valor solicitado sob a chave raiz, ele deve tentar recuperar o valor comparável da **\*** subchave.

 <span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER** 

Especifica que quando um método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) não encontra o valor solicitado sob a chave raiz, ele deve tentar recuperar o valor comparável da subchave **Folder** .

 <span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS** 

Especifica que somente **a \_ \_ raiz de classes hKey** deve ser pesquisada e que o **HKEY \_ Current \_ User** deve ser ignorado.

 <span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOtruncate** 

Especifica que a cadeia de caracteres de retorno não deve ser truncada. Em vez disso, retorne um valor de erro e o tamanho necessário para a cadeia de caracteres completa.

 <span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ verificar** 

Instrui os métodos [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) para verificar se os dados são precisos. Essa configuração permite que os métodos **IQueryAssociations** leiam dados do disco rígido do usuário para verificação. Por exemplo, eles podem verificar o nome amigável no registro em relação a um armazenado no arquivo. exe. Definir esse sinalizador normalmente reduz a eficiência do método.

 <span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL** 

Instrui os métodos [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) a ignorar Rundll.exe e retornar informações sobre seu destino. Normalmente, os métodos **IQueryAssociations** retornam informações sobre o primeiro. exe ou. dll em uma cadeia de caracteres de comando. Se um comando usa Rundll.exe, a definição desse sinalizador informa o método para ignorar Rundll.exe e retornar informações sobre seu destino.

 <span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOcorreções** 

Instrui os métodos [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) a não corrigir erros no registro, como o nome amigável de uma função que não corresponde a um encontrado no arquivo. exe.

 <span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS** 

Especifica que o valor de BaseClass deve ser ignorado.

 <span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN** 

**Introduzido no Windows 7**. Especifica que o ProgID "desconhecido" deve ser ignorado; em vez disso, falha.

 <span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_ \_ ProgID fixo ASSOCF \_ init** 

**Introduzido no Windows 8**. Especifica que o ProgID fornecido deve ser mapeado usando os padrões do sistema, em vez dos padrões do usuário atual.

 <span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ é \_ protocolo** 

**Introduzido no Windows 8**. Especifica que o valor é um protocolo e deve ser mapeado usando os padrões do usuário atual.

 <span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ para \_ arquivo** 

**Introduzido em Windows 8.1**. Especifica que o ProgID corresponde a uma associação baseada em extensão de arquivo. Use junto com o **ASSOCF \_ init \_ Fixed \_ ProgID**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]               |
| Servidor mínimo com suporte | Windows 2000 Server \[somente aplicativos da área de trabalho\]                                 |
| Cabeçalho                   |  Shlwapi. h  |



## <a name="see-also"></a>Confira também

 [**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) 

 

 

© 2017 Microsoft. Todos os direitos reservados.
