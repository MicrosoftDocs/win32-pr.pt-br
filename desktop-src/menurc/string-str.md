---
title: Estrutura da cadeia de caracteres
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas registradas.
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- Menus de estrutura de cadeia de caracteres e outros recursos
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796140"
---
# <a name="string-structure"></a>Estrutura da cadeia de caracteres

Representa a organização de dados em um recurso de versão de arquivo. Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas registradas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a>Membros

<dl> <dt>

**wLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O comprimento, em bytes, dessa estrutura de **cadeia de caracteres** .

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tamanho, em palavras, do membro de **valor** .

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

O tipo de dados no recurso de versão. Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Uma cadeia de caracteres Unicode arbitrária. O membro **szKey** pode ser um ou mais dos valores a seguir. Esses valores são apenas diretrizes.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Feitos**


</dt> <dd>

O membro de **valor** contém qualquer informação adicional que deve ser exibida para fins de diagnóstico. Essa cadeia de caracteres pode ter um comprimento arbitrário.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**


</dt> <dd>

O membro de **valor** identifica a empresa que produziu o arquivo. Por exemplo, "Microsoft Corporation" ou "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**


</dt> <dd>

O membro de **valor** descreve o arquivo de forma que ele possa ser apresentado aos usuários. Essa cadeia de caracteres pode ser apresentada em uma caixa de listagem quando o usuário estiver escolhendo os arquivos a serem instalados. Por exemplo, "driver de teclado para os teclados no estilo" ou "Microsoft Word para Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**


</dt> <dd>

O membro de **valor** identifica a versão deste arquivo. Por exemplo, o **valor** poderia ser "3,00 a" ou "5,00. RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**Internoname**


</dt> <dd>

O membro de **valor** identifica o nome interno do arquivo, se houver. Por exemplo, essa cadeia de caracteres pode conter o nome do módulo para uma DLL, um nome de dispositivo virtual para um dispositivo virtual do Windows ou um nome de dispositivo para um driver de dispositivo MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

O membro de **valor** descreve todos os avisos de direitos autorais, marcas registradas e marcas registradas que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, datas de direitos autorais, números de marca e assim por diante. Em inglês, essa cadeia de caracteres deve estar no formato "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**


</dt> <dd>

O membro de **valor** descreve todas as marcas registradas e marcas registradas que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, números de marca e assim por diante. Em inglês, essa cadeia de caracteres deve estar no formato "Windows is a trademark of Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

O membro de **valor** identifica o nome original do arquivo, sem incluir um caminho. Isso permite que um aplicativo determine se um arquivo foi renomeado por um usuário. Esse nome não pode ser MS-DOS 8,3 se o arquivo for específico para um sistema de arquivos não FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

O membro de **valor** descreve por quem, onde e por que esta versão particular do arquivo foi criada. Essa cadeia de caracteres só deverá estar presente se o sinalizador do **vs \_ FF \_ PRIVATEBUILD** estiver definido no membro **dwFileFlags** da estrutura do [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Por exemplo, o **valor** poderia ser "criado pela interface Oscar on \\ OSCAR2".

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**NomeDoProduto**


</dt> <dd>

O membro de **valor** identifica o nome do produto com o qual esse arquivo é distribuído. Por exemplo, essa cadeia de caracteres pode ser "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**


</dt> <dd>

O membro de **valor** identifica a versão do produto com a qual esse arquivo é distribuído. Por exemplo, o **valor** poderia ser "3,00 a" ou "5,00. RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**


</dt> <dd>

O membro de **valor** descreve como essa versão do arquivo difere da versão normal. Essa entrada só deverá estar presente se o sinalizador do **vs \_ FF \_ SPECIALBUILD** estiver definido no membro **dwFileFlags** da estrutura do [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Por exemplo, o **valor** poderia ser "compilação particular para a resolução de problemas de mouse em M250 e M250E Computers".

</dd> </dl> </dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Tantas palavras zero quantas forem necessárias para alinhar o membro de **valor** em um limite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Uma cadeia de caracteres terminada em zero. Consulte a descrição do membro **szKey** para obter mais informações.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura verdadeira de linguagem C porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de cabeçalho fornecidos com o SDK (Software Development Kit) do Windows.

Uma estrutura de **cadeia de caracteres** pode ter um valor de **szKey** de, por exemplo, "CompanyName" e um **valor** de "Microsoft Corporation". Outra estrutura de **cadeia de caracteres** com o mesmo valor de **szKey** pode conter um **valor** de "Microsoft GmbH". Isso pode ocorrer se a segunda estrutura de **cadeia de caracteres** estivesse associada a uma estrutura [**STRINGTABLE**](stringtable.md) cujo valor **szKey** seja 040704b0, alemão/Unicode.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**StringTable**](stringtable.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





