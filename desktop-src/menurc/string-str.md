---
title: Estrutura de cadeia de caracteres
description: Representa a organização de dados em um recurso de versão de arquivo. Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas comerciais.
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
ms.openlocfilehash: a6db2c10e981ae059a46e84e7abfc4d6dfc372fc3c75c76cfc20fd8a8f42735d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776726"
---
# <a name="string-structure"></a>Estrutura de cadeia de caracteres

Representa a organização de dados em um recurso de versão de arquivo. Ele contém uma cadeia de caracteres que descreve um aspecto específico de um arquivo, por exemplo, a versão de um arquivo, seus avisos de direitos autorais ou suas marcas comerciais.

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

Tipo: **WORD**

</dd> <dd>

O comprimento, em bytes, dessa estrutura **string.**

</dd> <dt>

**wValueLength**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O tamanho, em palavras, do **membro Value.**

</dd> <dt>

**wType**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

O tipo de dados no recurso de versão. Esse membro será 1 se o recurso de versão contiver dados de texto e 0 se o recurso de versão contiver dados binários.

</dd> <dt>

**szKey**
</dt> <dd>

Tipo: **WCHAR**

</dd> <dd>

Uma cadeia de caracteres Unicode arbitrária. O **membro szKey** pode ser um ou mais dos valores a seguir. Esses valores são apenas diretrizes.

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comentários**


</dt> <dd>

O **membro** Value contém informações adicionais que devem ser exibidas para fins de diagnóstico. Essa cadeia de caracteres pode ter um comprimento arbitrário.

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**Companyname**


</dt> <dd>

O **membro** Value identifica a empresa que produziu o arquivo. Por exemplo, "Microsoft Corporation" ou "Standard Microsystems Corporation, Inc."

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**Filedescription**


</dt> <dd>

O **membro** Value descreve o arquivo de forma que ele possa ser apresentado aos usuários. Essa cadeia de caracteres pode ser apresentada em uma caixa de listagem quando o usuário está escolhendo arquivos a serem instalados. Por exemplo, "Driver de teclado para teclados no estilo AT" ou "Microsoft Word para Windows".

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**Fileversion**


</dt> <dd>

O **membro** Value identifica a versão desse arquivo. Por exemplo, **Value** pode ser "3.00A" ou "5.00.RC2".

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**Internalname**


</dt> <dd>

O **membro** Value identifica o nome interno do arquivo, se houver um. Por exemplo, essa cadeia de caracteres pode conter o nome do módulo para uma DLL, um nome de dispositivo virtual para um Windows virtual ou um nome de dispositivo para um driver de dispositivo MS-DOS.

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**


</dt> <dd>

O **membro Valor** descreve todos os avisos de direitos autorais, marcas comerciais e marcas registradas que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, datas de direitos autorais, números de marca e assim por diante. Em inglês, essa cadeia de caracteres deve estar no formato "Copyright Microsoft Corp. 1990 1994".

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**Legaltrademarks**


</dt> <dd>

O **membro Value** descreve todas as marcas comerciais e marcas registradas que se aplicam ao arquivo. Isso deve incluir o texto completo de todos os avisos, símbolos legais, números de marca e assim por diante. Em inglês, essa cadeia de caracteres deve estar no formato "Windows is a trademark of Microsoft Corporation".

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**


</dt> <dd>

O **membro** Value identifica o nome original do arquivo, não incluindo um caminho. Isso permite que um aplicativo determine se um arquivo foi renomeado por um usuário. Esse nome poderá não ser o formato MS-DOS 8.3 se o arquivo for específico para um sistema de arquivos não FAT.

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**


</dt> <dd>

O **membro** Value descreve por quem, onde e por que essa versão privada do arquivo foi criada. Essa cadeia de caracteres só deverá estar presente se o sinalizador **\_ \_ PRIVATEBUILD** do VS FF estiver definido no **membro dwFileFlags** da estrutura [**VS \_ FIXEDFILEINFO.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Por exemplo, **Value** pode ser "Criado por PRÊMIO em \\ LTD2".

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**Productname**


</dt> <dd>

O **membro** Value identifica o nome do produto com o qual esse arquivo é distribuído. Por exemplo, essa cadeia de caracteres pode ser "Microsoft Windows".

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**Productversion**


</dt> <dd>

O **membro** Value identifica a versão do produto com a qual esse arquivo é distribuído. Por exemplo, **Value** pode ser "3.00A" ou "5.00.RC2".

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**Specialbuild**


</dt> <dd>

O **membro** Value descreve como essa versão do arquivo difere da versão normal. Essa entrada só deverá estar presente se o sinalizador **\_ \_ SPECIALBUILD** do VS FF estiver definido no **membro dwFileFlags** da estrutura [**VS \_ FIXEDFILEINFO.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Por exemplo, **Value pode** ser "Build privado para o Notebook resolvendo problemas do mouse em computadores M250 e M250E".

</dd> </dl> </dd> <dt>

**Preenchimento**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Quantas palavras zero necessárias para alinhar o **membro Value** em um limite de 32 bits.

</dd> <dt>

**Valor**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Uma cadeia de caracteres terminada em zero. Confira a **descrição do membro szKey** para obter mais informações.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é uma estrutura de linguagem C verdadeira porque contém membros de comprimento variável. Essa estrutura foi criada exclusivamente para representar a organização de dados em um recurso de versão e não aparece em nenhum dos arquivos de header fornecidos com o SDK (Software Development Kit) do Windows.

Uma **estrutura string** pode ter um valor **szKey** de, por exemplo, "CompanyName" e **um Valor** de "Microsoft Corporation". Outra **estrutura string** com o mesmo valor **szKey** pode conter **um Valor** de "Microsoft GmbH". Isso pode ocorrer se a segunda estrutura **String** estiver associada a uma estrutura [**StringTable**](stringtable.md) cujo valor **szKey** é 040704b0, ou seja, alemão/Unicode.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Stringtable**](stringtable.md)
</dt> <dt>

[**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[**StringFileInfo**](stringfileinfo.md)
</dt> <dt>

[**VS \_ VERSIONINFO**](vs-versioninfo.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Informações sobre versão](version-information.md)
</dt> </dl>

 

 





