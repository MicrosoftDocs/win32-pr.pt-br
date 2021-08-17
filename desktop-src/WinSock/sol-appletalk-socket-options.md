---
description: A tabela a seguir descreve as opções de soquete SOL APPLETALK que se aplicam a soquetes criados para a família de \_ endereços AppleTalk (AF \_ APPLETALK).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: SOL_APPLETALK opções de soquete (Atalkwsh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 5ea45b4007a3bd36d2cfbceda5b7ec4f2cff20d9bb2387fb2d184710a8a4492c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740003"
---
# <a name="sol_appletalk-socket-options"></a>Opções \_ de soquete SOL APPLETALK

A tabela a seguir descreve as opções de soquete **SOL \_ APPLETALK** que se aplicam a soquetes criados para a família de endereços AppleTalk (AF \_ APPLETALK). Consulte as páginas de referência da função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Opções \_ de soquete SOL APPLETALK**</dt> <dd> <dl> <dt> 

| Opção                          | Obter | Definir | Tipo de aceitação                          | Descrição                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PORTANTO, \_ CONFIRME \_ O NOME               | sim |     | **TUPLA \_ NBP do WSH \_**                  | Confirma se um determinado nome do AppleTalk está vinculado ao endereço determinado.                                                                                                                                  |
| PORTANTO, \_ NOME DO REGISTRO \_            |     | sim | **NOME DO REGISTRO \_ WSH \_**              | Desregula o nome da rede.                                                                                                                                                               |
| PORTANTO, \_ GETLOCALZONES               | sim |     | **ZONAS DE \_ LOOKUP \_ WSH**               | Retorna uma lista de nomes de zona conhecidos pelo nome do adaptador determinado.                                                                                                                                        |
| PORTANTO, \_ GETMYZONE                   | sim |     | Char \[\]                            | Retorna a zona padrão na rede.                                                                                                                                                             |
| PORTANTO, \_ GETNETINFO                  | sim |     | **WSH \_ LOOKUP \_ NETDEF \_ NO \_ ADAPTADOR** | Retorna os valores de semente para a rede, bem como a zona padrão. O *parâmetro optlen* deve ser pelo menos um byte maior que o tamanho da estrutura **WSH \_ LOOKUP \_ NETDEF \_ ON \_ ADAPTER.**  |
| PORTANTO, \_ GETZONELIST                 | sim |     | **ZONAS DE \_ LOOKUP \_ WSH**               | Retorna nomes de zona da lista de zonas da Internet. O *parâmetro optlen* deve ser pelo menos um byte maior que o tamanho da estrutura **WSH \_ LOOKUP \_ ZONES.**                                       |
| ENTÃO, \_ PROCURE \_ MYZONE              | sim |     |                                      | O mesmo que SO \_ GETMYZONE                                                                                                                                                                                |
| PORTANTO, \_ NOME DA \_ LOOKUP                | sim |     | **NOME DA LOOKUP DO WSH \_ \_**                | Procura um nome NBP especificado e retorna as tuplas correspondentes de nome e informações de NBP. O *parâmetro optlen* deve ser pelo menos um byte maior que o tamanho da estrutura WSH \_ LOOKUP \_ NAME. |
| PORTANTO, \_ PROCURE \_ NETDEF \_ NO \_ ADAPTADOR | sim |     | **WSH \_ LOOKUP \_ NETDEF \_ NO \_ ADAPTADOR** | O mesmo que SO \_ GETNETINFO.                                                                                                                                                                              |
| PORTANTO, \_ AS \_ ZONAS DE LOOKUP               | sim |     | **ZONAS DE \_ LOOKUP \_ WSH**               | O mesmo que SO \_ GETZONELIST.                                                                                                                                                                             |
| PORTANTO, \_ PROCURE \_ ZONAS \_ NO \_ ADAPTADOR  | sim |     | **ZONAS DE \_ LOOKUP \_ WSH**               | O mesmo que SO \_ GETLOCALZONES.                                                                                                                                                                           |
| PORTANTO, \_ O PAP OBTER STATUS DO \_ \_ \_ SERVIDOR    | sim |     | **WSH \_ PAP OBTER STATUS DO \_ \_ \_ SERVIDOR**    | Retorna o status de PAP de um determinado servidor                                                                                                                                                           |
| ENTÃO, \_ PAP \_ PRIME \_ READ            |     | sim | Char \[\]                            | Essa chamada é uma leitura em uma conexão PAP para que o remetente possa começar a enviar os dados                                                                                                                 |
| PORTANTO, \_ STATUS DO SERVIDOR DO CONJUNTO \_ \_ DE PAP \_    |     | sim | Char \[\]                            | Define o status a ser enviado se outro cliente solicitar o status                                                                                                                                     |
| PORTANTO, \_ \_ REGISTRE O NOME              |     | sim | **NOME DO REGISTRO \_ WSH \_**              | Registra o nome determinado na rede AppleTalk                                                                                                                                                    |
| PORTANTO, \_ REMOVA \_ O NOME                |     | sim | **NOME DO REGISTRO \_ WSH \_**              | O mesmo QUE SO \_ DEREGISTER \_ NAME                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows Suporte para opções \_ SOL APPLETALK**</dt> <dd> <dl> <dt> 

| Opção                          | Windows Vista e posterior | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| PORTANTO, \_ CONFIRME \_ O NOME               |                         | x                   | x          | x            | x           |               |
| PORTANTO, \_ NOME DO REGISTRO \_            |                         | x                   | x          | x            | x           |               |
| PORTANTO, \_ GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| \_GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| \_GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| Então \_ GETzonelist                 |                         | x                   | x          | x            | x           |               |
| Portanto, \_ pesquise \_ MyZone              |                         | x                   | x          | x            | x           |               |
| Então \_ , \_ nome da pesquisa                |                         | x                   | x          | x            | x           |               |
| Então, \_ pesquise o \_ NETDEF \_ no \_ adaptador |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ zonas de pesquisa               |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ zonas \_ de pesquisa no \_ adaptador  |                         | x                   | x          | x            | x           |               |
| Portanto, o \_ PAP \_ Obtém o \_ status do servidor \_    |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ Leia a linha PAP \_            |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ defina o \_ status do servidor do PAP \_    |                         | x                   | x          | x            | x           |               |
| Portanto \_ , \_ nome do registro              |                         | x                   | x          | x            | x           |               |
| Então, \_ Remover \_ nome                |                         | x                   | x          | x            | x           |               |



 

as opções de **SOL \_ APPLETALK** só têm suporte nas versões de servidor do Windows 2000 e Windows NT 4,0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

As opções de soquetes do sol e as estruturas usadas por essas opções de soquete são definidas no arquivo de cabeçalho *Atalkwsh. h* . **\_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Atalkwsh. h</dt> </dl> |



 

 




