---
title: Chave ProgID independente de versão
description: Associa um ProgID a um CLSID. Essa chave é usada para determinar a versão mais recente de um aplicativo de objeto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dec371f87ff3aba98bd642537e4de893df20682cc9bd84eda8829f24d241b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567966"
---
# <a name="version-independent-progid-key"></a>Chave ProgID independente de versão

Associa um ProgID a um CLSID. Essa chave é usada para determinar a versão mais recente de um aplicativo de objeto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Comentários

A **chave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde à chave **\_ \_ RAIZ de CLASSES HKEY,** que foi mantida para compatibilidade com versões anteriores do COM.

O formato para <*ProgID* independente de versão> é <programa *>.<* *componente*>, separado por períodos, sem espaços e sem número de versão. O ProgID independente de versão, como o ProgID, pode ser registrado com um nome acessível por humanos.

*ProgID* é o ProgID da versão instalada mais recente da classe .

Os aplicativos devem registrar um identificador programático independente de versão na chave *ProgID* independente de versão. O ProgID independente de versão refere-se à classe do aplicativo e não muda de versão para versão, em vez disso, permanece constante em todas as versões, por exemplo, Microsoft Word Document. Ele é usado com linguagens de macro e refere-se à versão instalada no momento da classe do aplicativo. O ProgID independente de versão deve corresponder ao nome da versão mais recente do aplicativo de objeto.

Por exemplo, o ProgID independente de versão é usado quando um aplicativo de contêiner cria um gráfico ou tabela com um botão de barra de ferramentas. Nessa situação, o aplicativo pode usar o ProgID independente de versão para determinar a versão mais recente do aplicativo de objeto necessário.

O ProgID independente de versão é armazenado e mantido exclusivamente pelo código do aplicativo. Quando dada a ProgID independente de versão, a [**função CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) retorna o CLSID da versão atual.

Você pode usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para converter entre essas duas representações.

Você pode usar [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) ou [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) para alterar o identificador para uma cadeia de caracteres exibivel.

Se um manipulador personalizado não for usado, a entrada deverá ser definida como OLE32.DLL, conforme mostrado no exemplo a seguir:

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<ProgID> Chave](-progid--key.md)
</dt> </dl>

 

 




